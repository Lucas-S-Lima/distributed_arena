# Distributed Arena 🎮

Um jogo da velha multiplayer executado em rede local, utilizando conceitos de computação distribuída e comunicação em tempo real via **WebSockets**.

---

## 📌 Sobre o Projeto

O objetivo deste projeto é permitir partidas de jogo da velha multiplayer entre dispositivos conectados na mesma rede local (LAN). Através de WebSockets, as ações dos jogadores e o estado do tabuleiro são sincronizados em tempo real, distribuindo a comunicação e o processamento entre os nós participantes.

---

## 🚀 Tecnologias

- **Python** (Django)
- **WebSockets** (comunicação bidirecional em tempo real)
- **HTML5 / CSS3 / JavaScript** (interface do usuário)

---

## 🛠️ Pré-requisitos

- [Python](https://www.python.org/) 3.10 ou superior
- Gerenciador de pacotes `pip`
- Ambiente virtual (`venv`)

---

## ⚙️ Instalação e Execução

### 1. Clonar o repositório
```bash
git clone <URL_DO_REPOSITORIO>
cd distributed_arena
```

### 2. Criar e ativar o ambiente virtual
```bash
# Criar ambiente virtual
python -m venv .venv

# Ativar no Linux/macOS:
source .venv/bin/activate

# Ativar no Windows:
# .venv\Scripts\activate
```

### 3. Instalar as dependências
```bash
pip install -r requirements.txt
```

### 4. Configurar variáveis de ambiente
Crie um arquivo `.env` na raiz do projeto (se ainda não existir) e defina a chave secreta:
```env
SECRET_KEY=sua-chave-secreta-aqui
```

### 5. Aplicar as migrações do banco de dados
```bash
python manage.py migrate
```

### 6. Iniciar o servidor na rede local
Para permitir conexões de outros dispositivos na mesma rede Wi-Fi/Ethernet, execute apontando para `0.0.0.0`:

```bash
python manage.py runserver 0.0.0.0:8000
```

> **Nota:** Certifique-se de adicionar o seu IP local ou `*` ao `ALLOWED_HOSTS` no `core/settings.py` caso necessário, e acesse pelo navegador em:
> `http://<SEU_IP_LOCAL>:8000`
