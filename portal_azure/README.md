# Resumo Completo do Portal Azure

## 1. Página Inicial (Dashboard)
- **Visão geral**: ao acessar `portal.azure.com`, você cai no dashboard padrão, com tiles de serviços usados recentemente, custo e notificações.  
- **Personalização**: arraste, redimensione e agrupe tiles para criar painéis dedicados (por ex. “Dev .NET”, “Infra de Rede”).

## 2. Configurações de Conta
No canto superior direito (ícone de engrenagem), ajuste:
- **Idioma e região**: defina Português (Brasil), English (US) etc., e fuso horário para relatórios.  
- **Tema e página de início**: escolha entre Claro, Escuro ou Colorido; e selecione se quer iniciar em Dashboard, Todos os serviços ou em um recurso específico.

## 3. Blade “Todos os Serviços”
- **Categorias principais**: Computação, Rede, Armazenamento, Banco de Dados, IA e ML, entre outras.  
- **Favoritos**: marque estrelas ⭐ para acesso rápido.  
- **Busca**: filtre escrevendo palavras-chave (ex.: “VM”, “Storage”) em tempo real.

## 4. Critérios de Organização por Categoria
O Azure Portal organiza cada família de serviços segundo o critério mais intuitivo para ela – nem sempre por IaaS/PaaS, mas às vezes por tipo ou função.  

| Categoria              | Critério de Organização                                                                                   |
|------------------------|-----------------------------------------------------------------------------------------------------------|
| Computação             | Modelo de entrega: IaaS (VMs, Discos), PaaS (App Service, SQL DB), Serverless (Functions, Logic Apps)     |
| Armazenamento          | Tipo de recurso: Blob, File, Queue, Table, Data Lake, Discos Gerenciados                                  |
| Rede                   | Função: Virtual Network, Load Balancer, Application Gateway, Firewall, CDN                                 |
| Banco de Dados         | Tecnologia ou padrão: SQL (Azure SQL DB), NoSQL (Cosmos DB), Cache (Redis), Analytics (Synapse)           |
| IA & Machine Learning  | Cenário: Visão computacional, linguagem, customização e frameworks (Cognitive Services, ML Studio)        |

> Em resumo, algumas categorias usam “modelo de serviço” (Computação), outras “tipo de dado” (Armazenamento) ou “função” (Rede), para facilitar a escolha.

## 5. Versões Preview e SLA
- Serviços em **Preview** vêm com selo “Preview”.  
- **Sem SLA garantido**: use-os para testes e feedback, mas evite em produção crítica.

---

## Próximos Passos
1. **Grupos de Recursos & Tags**: organização e controle de custos.  
2. **RBAC**: permissões finas para usuários e identidades de serviço.  
3. **Políticas & Blueprints**: padronização e compliance.  
4. **Cost Management**: alertas de orçamento e relatórios.  
5. **Cloud Shell / CLI**: automação via linha de comando no navegador.  
6. **Azure Advisor**: recomendações de segurança, performance e custo.

