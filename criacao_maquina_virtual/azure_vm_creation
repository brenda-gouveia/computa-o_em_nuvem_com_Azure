## Guia: Como Criar uma Máquina Virtual com Azure CLI

---

### 🔧 Pré-requisitos

1. Conta Azure ativa
2. Azure CLI instalada

   * [Guia oficial de instalação](https://learn.microsoft.com/pt-br/cli/azure/install-azure-cli)
3. Fazer login:

```bash
az login
```

---

### 🧱 1. Criar um Grupo de Recursos

```bash
az group create \
  --name meu-grupo \
  --location eastus
```

* `--name`: nome do grupo
* `--location`: região (ex: `eastus`, `brazilsouth`, etc.)

---

### 💻 2. Criar a Máquina Virtual

```bash
az vm create \
  --resource-group meu-grupo \
  --name minha-vm \
  --image UbuntuLTS \
  --size Standard_B1s \
  --admin-username azureuser \
  --generate-ssh-keys
```

**Parâmetros importantes:**

* `--image`: Sistema operacional (ex: `UbuntuLTS`, `Windows2022`)
* `--size`: Tipo de VM (ex: `Standard_B1s`)
* `--generate-ssh-keys`: cria par de chaves SSH (armazenadas em `~/.ssh/`)

---

### 🔓 3. Acessar a VM via SSH

```bash
ssh azureuser@<ip-publico>
```

Exemplo:

```bash
ssh azureuser@20.66.37.82
```

---

### 📄 4. (Opcional) Abrir Porta no Firewall (NSG)

Exemplo: liberar porta 80 (HTTP):

```bash
az vm open-port \
  --port 80 \
  --resource-group meu-grupo \
  --name minha-vm
```

---

### ✅ Resumo Visual dos Comandos

```bash
# Login
az login

# Criar grupo de recursos
az group create --name meu-grupo --location eastus

# Criar VM
az vm create \
  --resource-group meu-grupo \
  --name minha-vm \
  --image UbuntuLTS \
  --size Standard_B1s \
  --admin-username azureuser \
  --generate-ssh-keys

# Abrir porta
az vm open-port --port 80 --resource-group meu-grupo --name minha-vm

# Acessar via SSH
ssh azureuser@<ip-publico>
```
