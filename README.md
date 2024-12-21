# Desafio Técnico - Desenvolvedor Pleno/Sênior

## Objetivo


Avaliar as habilidades técnicas e boas práticas no desenvolvimento de sistemas com foco em organização, eficiência e escalabilidade. Este desafio simula um caso real onde você criará um sistema para gerenciamento e exibição de dados de clientes e compromissos.


## Descrição do Desafio

Parte Administrativa (Painel)

### Acesso ao Painel:
O painel administrativo deve ser protegido por autenticação via e-mail e senha.

### Funcionalidades do Painel:

#### Importação de CSV:
Permita o upload de um arquivo CSV chamado clientes.csv (enviado em anexo), contendo os seguintes campos:

| Nome | Endereço | Cidade | Estado | CEP |  Telefone | CPF |
| ------------- | ---------------- | --------- | -- | --------- | --------------- | -------------- |
  
Os dados do CSV não estão normalizados. É necessário:

- Padronizar os nomes (ex.: capitalizar corretamente, remover caracteres desnecessários).
- Dividir o endereço em Endereço, Cidade, Estado e CEP no formato correto.
- Normalizar os telefones no formato: (XX) XXXX-XXXX ou (XX) XXXXX-XXXX.
- Formatá-los CPFs no padrão: XXX.XXX.XXX-XX.
- Não deve importar cliente se o CPFs já existir na base.
- Após a normalização, os dados devem ser salvos na base no seguinte formato:

| Fulano de Tal | Rua das Coves 35 | São Paulo | SP | 36026-500 |  (11) 3216-2035 | 071.020.298-24 |
| ------------- | ---------------- | --------- | -- | --------- | --------------- | -------------- |

#### Formulário de Inclusão Manual:
- Crie um formulário que permita a inclusão manual de novos clientes no painel administrativo (além da importação de csv).
- Campos obrigatórios: Nome, Endereço, Cidade, Estado, CEP, Telefone e CPF.
  - Não deve cadastrar se o CPFs já existir na base.

- Listagem de clientes:
  - Criar uma tabela para listar clientes cadastrados.
  - Permitir busca por CPF, Nome ou Telefone.
  - Paginação e ordenação por Nome, Estado ou Data de Cadastro.
- Compromissos
- Cadastrar compromissos com:
  - Nome do compromisso.
  - Data de início e fim.
- Regras:
  - Não permitir o cadastro de compromissos com conflitos de horário.
  - Exibir mensagens claras em caso de erro.
- Criar uma tabela para listar compromissos


### Parte Externa (Pública)

Acesse esta parte diretamente pela raiz do domínio (não exige autenticação).<br>
Ela deve exibir em tempo real as seguintes informações:

- Quantidade total de clientes cadastrados.
- Quantidade de clientes com telefone duplicados.
- Quantidade de clientes por estado.

> [!NOTE]
> Nota: A atualização deve ser dinâmica (ex.: usando WebSocket ou AJAX).

## Requisitos Técnicos

- Linguagem e ferramentas: Escolha a linguagem e os frameworks que preferir.<br>
- Base de dados: Utilize um banco de dados relacional como MySQL ou PostgreSQL.<br>
- Servidor: Suba o projeto em um ambiente de produção (ex.: AWS, Heroku, etc.), tornando-o acessível para avaliação.

## O que será avaliado

1. Organização e clareza do código: Estrutura limpa e bem documentada.
2. Normalização dos dados: Tratamento adequado dos dados do CSV.
3. Funcionalidade e interface: Usabilidade do painel administrativo e exibição precisa na página pública.
4. Atualização em tempo real: Qualidade e eficiência na implementação da contagem dinâmica.
5. Deploy: Facilidade de configuração e acesso ao sistema.

## Entrega

- Envie o link do sistema em produção.<br>
- Inclua um repositório (GitHub ou GitLab) contendo o código-fonte com README explicando:<br>
  - Como rodar o projeto localmente.
  - Como acessar o painel (login e senha).
  - Explicação sobre as principais escolhas técnicas.

## Bônus

- Testes automatizados cobrindo as funcionalidades principais.
- Boas práticas de segurança, como proteção contra injeções SQL e validação de entradas.
- Utilizar workers ou fila para processar o CSV em background

Envie o link do repositório para o email gustavo@codental.com.br com o assunto "Desafio Técnico <seu nome>"<br>
O prazo para entrega é 7 dias.

Boa sorte! Estamos ansiosos para avaliar o seu trabalho. 💻
