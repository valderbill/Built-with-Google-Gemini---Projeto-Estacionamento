# Sistema de Estacionamento

Aplicação em Python para controle de entrada e saída de veículos em um estacionamento, com separação de vagas por tipo (`carro`, `moto` e `pcd`).

> Built with Google Gemini

## Funcionalidades

- Registro de entrada de veículos por placa e tipo.
- Validação de capacidade por categoria de vaga.
- Registro de saída com cálculo de tempo de permanência.
- Exibição de status geral de ocupação e vagas disponíveis.
- Listagem de veículos ativos e histórico de veículos que já saíram.

## Regras do sistema

- Tipos aceitos: `carro`, `moto`, `pcd`.
- Não permite entrada duplicada para veículo que já está no estacionamento.
- Não permite entrada quando a categoria de vaga estiver lotada.
- Ao registrar saída, o veículo é removido da lista ativa e vai para o histórico.

## Estrutura atual

- `sistema_estacionamento.py`: código principal com classes e menu interativo.
  - `Veiculo`: representa dados de placa, tipo, hora de entrada e saída.
  - `Estacionamento`: gerencia vagas, veículos ativos, histórico e operações.
  - `menu()`: interface de terminal para interação com o usuário.

## Capacidade padrão de vagas

- Carros: 50
- Motos: 20
- PCD: 10

## Como executar

### Pré-requisitos

- Python 3.8 ou superior

### Criando ambiente virtual (recomendado)

No PowerShell, dentro da pasta do projeto:

```powershell
python -m venv .venv
\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

### Execução

No terminal, dentro da pasta do projeto:

```bash
python sistema_estacionamento.py
```

## Menu disponível

1. Registrar Entrada
2. Registrar Saída
3. Exibir Status
4. Listar Veículos
5. Sair

## Exemplo rápido de uso

Fluxo básico no terminal:

1. Escolha `1` (Registrar Entrada)
2. Informe placa, por exemplo: `ABC1234`
3. Informe tipo: `carro`
4. Escolha `3` (Exibir Status) para ver ocupação atual
5. Escolha `2` (Registrar Saída) e informe a mesma placa
6. Escolha `4` (Listar Veículos) para ver ativos e histórico

## Melhorias futuras (opcional)

- Persistência em arquivo ou banco de dados.
- Cálculo de cobrança por tempo de permanência.
- Testes automatizados para regras de negócio.
- Interface gráfica ou API web.
