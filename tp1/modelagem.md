## Especificação dos Requisitos e Modelo Conceitual
### Minimundo:
É necessário a construção de um sistema que facilite a integração de novos integrantes de organizações usando cursos e capacitações da organização. Esse sistema vai servir para qualquer tipo de organização: empresas, instituições públicas, universidades. E por isso é preciso ter um administrador da organização para controlar partes do sistema.

O administrador terá acesso a criação de departamentos e a designação de gerentes do departamento.

Os gerentes dos departamentos poderão administrar somente 1 departamento e poderão criar cursos e designar professores.

O novo integrante será associado a somente um departamento, e assim irá ter acesso aos cursos ofertados por aquele departamento.

Como forma de fomento a realização dos cursos, terá um ranking de conhecimento baseado na quantidade de cursos concluidos entre os integrantes de todos os departamentos.

### Tabela de Requisitos do Banco de Dados:
| #RBD  | Nome RBD                                            | Descrição RBD                                                                                                                                                |
| ----- | --------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| RBD01 | Armazenar as informações da organização             | Armazenar os atributos da organização que irá usar o sistema (nome, tipo, quando foi criada, administrador que gerencia a organização)                       |
| RBD02 | Amazenar as informações do administrador do sistema | Armazenar os atributos do administrador do sistema (nome, cpf, data de nascimento)                                                                           |
| RBD03 | Armazenar os departamentos e seus atributos         | Armazenar cada departamento da organização (codigo do departamento, nome, gerente do departamento)                                                           |
| RBD04 | Armazenar os gerentes dos departamentos             | Armazenar os gerentes dos departamentos com sua designação (nome, cpf, data de nascimento)                                                                   |
| RBD05 | Armazenar os cursos de cada departamento            | Armazenar os cursos de cada departamento (código do curso, nome, carga horária, departamento que ele está incluido, professor que leciona)                   |
| RBD06 | Armazenar os professores de cada curso              | Armazenar os professores de cada curso, associando qual curso que leciona (nome, cpf, data de nascimento)                                                    |
| RBD07 | Armazenar os integrantes da instituição             | Armazenar os integrantes da organização, com sua associação com o departamento (nome, cpf, data de nascimento, departamento que ele está incluido)           |
| RBD08 | Armazenar o ranking de conhecimento                 | Armazenar o ranking de conhecimento dos integrantes (cpf do integrante, quantidade de cursos concluidos, posição no ranking)                                 |
| RBD09 | Armazenar o progresso dos cursos dos integrantes    | Armazenar o progresso dos cursos feitos pelos integrantes(entidade fraca) (cpf do integrande, curso que está estudando, progresso, concluido(True or False)) |

### Regras de negócio:
- A Organização só pode ter 1 Administrador
- A Organização pode ter N Departamentos
- Somente o Administrador pode criar Departamentos
- O Administrador não pode criar cursos
- Cada um dos Departamentos só podem ter 1 Gerente
- Cada Departamento pode ter N Integrantes
- Cada Departamento pode ter N Cursos
- Cada Curso pode ter somente 1 Professor
- Um Professor também é um Integrante
- Cada Integrante pode fazer N Cursos
- Cada Integrante tem que está em somente 1 Departamento


## MER (texto/tabela com entidades, atributos, chaves, relacionamentos, regras)



## DER (imagem legível, notação Chen ou Crow’s Foot)



## Esquema Relacional (tabelas, colunas, PK/FK, observações)



## Normalização (DFs + 1FN/2FN/3FN com justificativa)



## Amostra mínima de dados (5–10 tuplas relevantes) em formato de tabela



## 3–5 consultas em linguagem natural que o BD deve responder