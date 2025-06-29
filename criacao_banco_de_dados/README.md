## Guia: Criar uma Instância SQL no Portal do Azure

---

### ✅ 1. Acessar o Portal

* Acesse: [https://portal.azure.com](https://portal.azure.com)
* Faça login com sua conta Azure.

---

### 📂 2. Criar um Banco de Dados SQL

1. Clique em **"Criar um recurso"**.
2. Vá para **"Banco de Dados" > "Banco de Dados SQL"**.
3. Clique em **"Criar"**.

---

### 📅 3. Preencher Detalhes

#### Aba: **Informações Básicas**

* **Assinatura**: escolha sua assinatura.
* **Grupo de recursos**: selecione ou crie um novo.
* **Nome do banco de dados**: ex: `meubanco`.
* **Servidor**: clique em “Criar novo”:

  * Nome do servidor (único)
  * Nome do administrador
  * Senha e confirmação
  * Região (ex: `Brazil South`)

> ✅ O servidor criado é a instância SQL propriamente dita.

---

### ⚙️ 4. Configurar Computação + Armazenamento

* Clique em **"Configurar banco de dados"**.
* Selecione um plano:

  * **Uso leve/testes**: `Basic` ou `5 DTUs`
  * **Uso avançado**: `vCore`
* Clique em **"Aplicar"**.

---

### 🔐 5. Configurar Rede

* Aba **"Rede"**:

  * Selecione **"Acesso público"**.
  * Marque **"Adicionar meu endereço IP atual"**.

---

### ⛨ 6. Configurações Adicionais (opcional)

* Collation personalizada (se desejar)
* Backup, geo-replicação, etc. (para ambientes produtivos)

---

### ✅ 7. Revisar e Criar

* Clique em **"Revisar + Criar"**.
* Valide as configurações.
* Clique em **"Criar"**.

---

### ⚙️ 8. Acessar a Instância e Conectar

1. No menu lateral: **"SQL Servers"**.
2. Selecione o servidor criado.
3. Copie o **nome do host** (ex: `servidor.database.windows.net`).
4. Conecte via:

   * **Azure Data Studio**
   * **SQL Server Management Studio (SSMS)**
   * Ou app com string de conexão

---

### 📂 Exemplo de String de Conexão

```txt
Server=tcp:servidor.database.windows.net,1433;Initial Catalog=meubanco;Persist Security Info=False;User ID=azureadmin;Password=SuaSenhaAqui;MultipleActiveResultSets=False;Encrypt=True;TrustServerCertificate=False;Connection Timeout=30;
```

---

> ℹ️ Dica: use **camadas gratuitas ou básicas** se estiver apenas testando para evitar cobranças desnecessárias.

---

## 🧠 Diferença entre Azure SQL Database e Azure SQL Managed Instance

| Característica                     | Azure SQL Database                        | Azure SQL Managed Instance                     |
| ---------------------------------- | ----------------------------------------- | ---------------------------------------------- |
| **Tipo de Serviço**                | Plataforma como Serviço (PaaS)            | Plataforma como Serviço (PaaS)                 |
| **Controle sobre a instância**     | Controla só o banco individual            | Controla a instância (vários bancos)           |
| **Compatibilidade com SQL Server** | Parcial (nem tudo do SQL Server funciona) | Alta (quase 100% compatível com local)         |
| **Acesso à rede VNet**             | Opcional, geralmente com IP público       | Obrigatório usar VNet (rede privada)           |
| **Migração Lift and Shift**        | Limitada                                  | Suporta migração direta de SQL Server local    |
| **Recursos do SQL Agent / Jobs**   | Não disponíveis                           | Disponíveis                                    |
| **Cross-database queries**         | Limitadas                                 | Suportadas                                     |
| **Preço**                          | Mais barato, ideal para apps isolados     | Mais caro, voltado para ambientes corporativos |
| **Modelo de cobrança**             | Por banco (DTU ou vCore)                  | Por instância (vCore)                          |

---

### 🎯 Casos de Uso

* **Azure SQL Database**

  * Aplicações web modernas
  * Projetos leves a médios
  * Sem necessidade de recursos avançados do SQL Server

* **Azure SQL Managed Instance**

  * Migração de sistemas legados (on-premise)
  * Precisa de SQL Agent, jobs, linked servers
  * Alta compatibilidade com SQL Server tradicional

---

### 📌 Exemplo Prático

| Situação                                    | Melhor escolha             |
| ------------------------------------------- | -------------------------- |
| Aplicativo novo com banco simples           | Azure SQL Database         |
| Migração de banco corporativo do SQL Server | Azure SQL Managed Instance |
| Precisa de jobs automatizados no SQL Agent  | Azure SQL Managed Instance |
| Aplicação com apenas 1 banco de dados       | Azure SQL Database         |

