# Cloud Cost Calculator 💰☁️

Uma calculadora profissional de custos multicloud para AWS, Azure e GCP com comparação em tempo real e relatórios corporativos avançados.

![Cloud Cost Calculator](https://img.shields.io/badge/Cloud-Calculator-blue)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-43853D?logo=node.js&logoColor=white)

## 🚀 Funcionalidades

- ✅ **Comparação Multicloud**: AWS, Azure e Google Cloud Platform
- ✅ **Tipos de Recursos**: Compute, Storage, Database, Network, Load Balancer
- ✅ **Preços Reais**: Integração com APIs oficiais das clouds
- ✅ **Cálculos Avançados**: Descontos, instâncias reservadas, multiplicadores regionais
- ✅ **Exportação**: Relatórios em PDF e CSV profissionais
- ✅ **Histórico**: Salvar e carregar estimativas anteriores
- ✅ **Gráficos**: Visualizações interativas de comparação
- ✅ **Templates**: Configurações rápidas para cenários comuns

## 🏗️ Arquitetura

### Frontend
- **React 18** com TypeScript
- **Tailwind CSS** + shadcn/ui para interface moderna
- **TanStack Query** para gerenciamento de estado
- **Recharts** para visualizações
- **React Hook Form** + Zod para formulários

### Backend
- **Express** + TypeScript
- **APIs das Clouds**: AWS Pricing, Azure Retail Prices, GCP Billing
- **Sistema de Cache** em memória com atualizações automáticas
- **Cron Jobs** para sincronização de preços

## 📦 Instalação

### Pré-requisitos
- Node.js 18+
- npm ou yarn

### Setup Local

```bash
# Clone o repositório
git clone https://github.com/arcegu1711/Cloudcalc.git
cd Cloudcalc

# Instale as dependências
npm install

# Inicie o servidor de desenvolvimento
npm run dev
```

A aplicação estará disponível em `http://localhost:5000`

## 🔑 Configuração das APIs

Para obter dados reais das clouds, configure as seguintes variáveis de ambiente:

### AWS Pricing API
```bash
AWS_ACCESS_KEY_ID=sua_access_key
AWS_SECRET_ACCESS_KEY=sua_secret_key
```

### Azure Retail Prices API
```bash
AZURE_SUBSCRIPTION_ID=sua_subscription_id
```

### Google Cloud Billing API
```bash
GOOGLE_CLOUD_PROJECT_ID=seu_project_id
```

## 📊 Providers Suportados

### AWS (Amazon Web Services)
- **Compute**: EC2 (t3, m5, c5, r5 families)
- **Storage**: EBS (gp3, io2, st1)
- **Database**: RDS (MySQL, PostgreSQL, SQL Server)
- **Network**: VPC, NAT Gateway, VPN
- **Load Balancer**: ALB, NLB, CLB

### Azure (Microsoft)
- **Compute**: Virtual Machines (B, D, F series)
- **Storage**: Managed Disks (Standard, Premium)
- **Database**: SQL Database, MySQL, PostgreSQL
- **Network**: Virtual Network, VPN Gateway
- **Load Balancer**: Application Gateway, Load Balancer

### GCP (Google Cloud)
- **Compute**: Compute Engine (e2, n1, c2 families)
- **Storage**: Persistent Disk (Standard, SSD)
- **Database**: Cloud SQL (MySQL, PostgreSQL)
- **Network**: VPC, Cloud VPN
- **Load Balancer**: HTTP(S), Network Load Balancer

## 🎯 Como Usar

1. **Selecione o Provider**: Escolha entre AWS, Azure ou GCP
2. **Configure Recursos**: Defina tipo de instância, região, quantidade
3. **Ajuste Parâmetros**: SO, storage, horas de uso, descontos
4. **Compare Preços**: Veja comparação automática entre providers
5. **Exporte Relatórios**: Gere PDFs ou CSVs para aprovações
6. **Salve Estimativas**: Histórico para reutilização futura

## 📈 Exemplos de Preços

### Cenário: Aplicação Web Pequena
- **AWS**: t3.medium (2 vCPUs, 4GB RAM) = $30.34/mês
- **Azure**: B2s (2 vCPUs, 4GB RAM) = $30.34/mês
- **GCP**: e2-medium (1 vCPU, 4GB RAM) = $24.41/mês

### Cenário: Banco de Dados Produção
- **AWS**: db.r5.xlarge + 500GB = $285.30/mês
- **Azure**: GP_Gen5_4 + 500GB = $267.45/mês
- **GCP**: db-n1-highmem-4 + 500GB = $245.12/mês

## 🔧 Scripts Disponíveis

```bash
# Desenvolvimento
npm run dev          # Inicia servidor de desenvolvimento

# Build
npm run build        # Gera build de produção
npm run preview      # Preview do build

# Qualidade
npm run lint         # Executa ESLint
npm run type-check   # Verifica tipos TypeScript
```

## 📂 Estrutura do Projeto

```
├── client/                 # Frontend React
│   ├── src/
│   │   ├── components/     # Componentes reutilizáveis
│   │   ├── hooks/         # Custom hooks
│   │   ├── lib/           # Utilitários
│   │   └── pages/         # Páginas da aplicação
│
├── server/                # Backend Express
│   ├── pricing/           # Integrações com APIs das clouds
│   ├── routes.ts          # Rotas da API
│   └── storage.ts         # Persistência de dados
│
├── shared/                # Código compartilhado
│   └── schema.ts          # Tipos e validações
│
└── docs/                  # Documentação
    ├── ARQUITETURA_APLICACAO.md
    └── PROBLEMAS_APLICACAO.md
```

## 🤝 Contribuindo

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📝 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para detalhes.

## 🆘 Suporte

- 📧 Email: suporte@cloudcalc.com
- 🐛 Issues: [GitHub Issues](https://github.com/arcegu1711/Cloudcalc/issues)
- 📖 Documentação: [Wiki do Projeto](https://github.com/arcegu1711/Cloudcalc/wiki)

## 🙏 Agradecimentos

- AWS, Azure e GCP pelas APIs públicas de preços
- Comunidade open source pelas bibliotecas utilizadas
- Contribuidores que ajudaram no desenvolvimento

---

Feito com ❤️ para a comunidade cloud