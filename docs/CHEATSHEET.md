# Aula 07 - Observabilidade Cheatsheet

## Grafana

```bash
docker run -d --name grafana -p 3000:3000 grafana/grafana:latest
```

- URL: http://localhost:3000
- User: admin / admin

## CloudTrail CLI

```bash
aws cloudtrail lookup-events \
  --lookup-attributes AttributeKey=EventSource,AttributeValue=ecs.amazonaws.com \
  --profile fiapaws
```

## Git Auditoria

```bash
git log --oneline -10
git blame arquivo.py
git show SHA
```

## SLSA Levels

| Level | Descrição |
|-------|-----------|
| 1 | Documentação |
| 2 | Build automatizado |
| 3 | Build isolado |
| 4 | Build hermético |

## Maturidade DevSecOps

| Nível | Foco |
|-------|------|
| 1 | CI/CD básico |
| 2 | SAST + SCA |
| 3 | Container + IaC |
| 4 | DAST + Centralização |
| 5 | Champions + Melhoria |

## Métricas Chave

- Mean Time to Detect (MTTD)
- Mean Time to Remediate (MTTR)
- SLA Compliance %
- Critical Backlog = 0
