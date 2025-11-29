# Aula 07 - Observabilidade e Maturidade DevSecOps

## 🎯 Objetivo

Implementar visualização de métricas, auditoria e apresentar roadmap de maturidade DevSecOps.

## 📹 Vídeos desta Aula

| Vídeo | Tema | O que você vai fazer |
|-------|------|---------------------|
| 01 | Grafana | Visualização de métricas de segurança |
| 02 | Auditoria | CloudTrail, GitHub logs, SLSA |
| 03 | Roadmap | Modelo de maturidade corporativa |

## 📁 Estrutura do Repositório

```
.
├── grafana/
│   ├── docker-compose.yml              # Container Grafana
│   ├── dashboards/
│   │   └── devsecops-dashboard.json    # Dashboard pronto para importar
│   └── provisioning/
│       ├── datasources/
│       │   └── defectdojo.yml          # Conexão com DefectDojo
│       └── dashboards/
│           └── default.yml
├── docs/
│   └── HANDS-ON-07-*.md
└── README.md
```

## ⚙️ Pré-requisitos

- [ ] Aula 06 concluída (DefectDojo com findings)
- [ ] Docker instalado

## 📚 Documentação

| Vídeo | Hands-on |
|-------|----------|
| 01 - Grafana | [HANDS-ON-07-01.md](docs/HANDS-ON-07-01.md) |
| 02 - Auditoria | [HANDS-ON-07-02.md](docs/HANDS-ON-07-02.md) |
| 03 - Roadmap | [HANDS-ON-07-03.md](docs/HANDS-ON-07-03.md) |

**Referência rápida**: [Cheatsheet](docs/CHEATSHEET.md)

---

**FIAP - Pós Tech DevSecOps**
