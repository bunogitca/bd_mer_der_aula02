# bd_mer_der_aula02
## Markdown

| Nome do Campo | Tipo de Dado | Tamanho | Restrições | Descrição |
| :--- | :--- | :---: | :--- | :--- |
| `id_paciente` | INT | Auto-incremento | **PK**, Not Null | Identificador único do paciente |
| `nome` | VARCHAR | 100 | Not Null | Nome completo do paciente |
| `cpf` | VARCHAR | 11 | Unique, Not Null | CPF (apenas números) |
| `data_nascimento` | DATE | - | Not Null | Data de nascimento do paciente |
| `telefone` | VARCHAR | 15 | Not Null | Telefone com DDD |
| `email` | VARCHAR | 100 | Null | E-mail para contato |


| Nome do Campo | Tipo de Dado | Tamanho | Restrições | Descrição |
| :--- | :--- | :---: | :--- | :--- |
| `id_medico` | INT | Auto-incremento | **PK**, Not Null | Identificador único do médico |
| `nome` | VARCHAR | 100 | Not Null | Nome completo do médico |
| `crm` | VARCHAR | 20 | Unique, Not Null | Registro do Conselho Regional de Medicina |
| `especialidade` | VARCHAR | 50 | Not Null | Especialidade médica |
| `telefone` | VARCHAR | 15 | Null | Telefone com DDD |
| `email` | VARCHAR | 100 | Null | E-mail profissional |


| Nome do Campo | Tipo de Dado | Tamanho | Restrições | Descrição |
| :--- | :--- | :---: | :--- | :--- |
| `id_consulta` | INT | Auto-incremento | **PK**, Not Null | Identificador único da consulta |
| `data` | DATE | - | Not Null | Data agendada para a consulta |
| `hora` | TIME | - | Not Null | Horário agendado para a consulta |
| `status` | VARCHAR | 20 | Not Null | Status: 'Agendada', 'Realizada', 'Cancelada' |
| `id_paciente` | INT | - | **FK**, Not Null | Código do paciente (Vem de T_PACIENTE) |
| `id_medico` | INT | - | **FK**, Not Null | Código do médico (Vem de T_MEDICO) |

## MER DER
![IMagem do MER DER](MER_DER.drawio.png)
## Dados de teste
[Paciente](<Book 3(Planilha1) (1).csv>)<br>
[Médico](<Book 3(Planilha3).csv>)<br>
[Consulta](<Book 3(Planilha4).csv>)