# 📊 Grafana + DefectDojo

Setup do Grafana com dashboard pré-configurado para visualizar métricas do DefectDojo.

## 📁 Estrutura

```
grafana/
├── docker-compose.yml          # Container do Grafana
├── dashboards/
│   └── devsecops-dashboard.json  # Dashboard pronto para uso
└── provisioning/
    ├── datasources/
    │   └── defectdojo.yml      # Configuração do datasource
    └── dashboards/
        └── default.yml         # Provisioning de dashboards
```

## 🚀 Quick Start

### 1. Pré-requisitos

- Docker instalado
- DefectDojo rodando na porta 8080 (aula 06)

### 2. Obter API Key do DefectDojo

1. Acesse: http://localhost:8080/api/key-v2
2. Copie o token

### 3. Configurar o Datasource

Edite o arquivo `provisioning/datasources/defectdojo.yml`:

```yaml
secureJsonData:
  httpHeaderValue1: "Token SEU_TOKEN_AQUI"  # <- Substitua aqui
```

### 4. Subir o Grafana

```bash
docker-compose up -d
```

### 5. Acessar

- **URL**: http://localhost:3000
- **Usuário**: `admin`
- **Senha**: `admin123`

O dashboard "DevSecOps Security Dashboard" já estará disponível!

## 🖥️ Dashboard

O dashboard inclui:

| Painel | Descrição |
|--------|-----------|
| 🔓 Total de Vulnerabilidades | Contagem total de findings ativos |
| 🚨 Críticos Abertos | Alerta visual (verde = 0, vermelho > 0) |
| 🟠 High | Vulnerabilidades de alta severidade |
| 🟡 Medium | Vulnerabilidades de média severidade |
| 📊 Por Severidade | Gráfico de pizza |
| 🛠️ Por Ferramenta | Gráfico de barras (Horusec, Trivy, ZAP) |
| 📋 Últimas Vulnerabilidades | Tabela com detalhes |

## 🔧 Troubleshooting

| Problema | Solução |
|----------|---------|
| Dashboard sem dados | Verificar se o DefectDojo está rodando |
| Erro de conexão | Verificar API Key no datasource |
| Linux: host.docker.internal não funciona | Usar `172.17.0.1` no datasource |

## 🔄 Importar Dashboard Manualmente

Se preferir importar manualmente:

1. Grafana > **Dashboards** > **Import**
2. Upload do arquivo `dashboards/devsecops-dashboard.json`
3. Selecione o datasource `DefectDojo`
4. Clique **Import**
