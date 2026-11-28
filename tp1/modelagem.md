## Especificação dos Requisitos e Modelo Conceitual
### Minimundo:
O minimundo é descrito como uma organização (privada ou pública) que deseja organizar e gerenciar de forma mais efetiva a integração de novos integrantes. A organização pode ter vários setores (departamentos, coordenação, diretorias etc.) que podem estar vinculados e gerenciar recursos e infraestrutura.

Todos os membros possuem um vínculo institucional com pelo menos um setor. Membros veteranos podem atuar como mentores, acompanhando novos integrantes durante o período de adaptação. Para cada perfil de ingresso, a organização define etapas de integração: leituras, treinamentos e tarefas práticas.

É necessário a construção de um sistema que facilite a integração de novos integrantes de organizações reduzindo o tempo e a dificuldade de adaptação.
O sistema deve oferecer:

* Um mapeamento da estrutura da organização, como hierarquia de setores e/ou departamentos e seus responsáveis;

* Informações sobre a organização dos fluxos internos (processos administrativos, acesso a sistemas etc.);
* Vincular o novo membro a um tutor ou chefe de departamento/setor para direcionar e sanar dúvidas relacionadas ao departamento/setor;
* Apresentar roteiros das atividades obrigatórias conforme perfil do novo integrante, permitindo acompanhar prazos e obrigações.

Esse sistema vai servir para qualquer tipo de organização: empresas, instituições públicas, universidades. E por isso é preciso ter um administrador da organização para controlar partes do sistema.

O administrador terá acesso a criação de departamentos e a designação de gerentes do departamento.

Os gerentes dos departamentos poderão administrar somente 1 departamento e poderão desguinar tutores criar treinamentos e atividades práticas, assim como, avaliar a evolução dos novos integrantes.

Um único tutor poderá acompanhar mais de um novo integrante daquele departamento/setor.

O novo integrante será associado a somente um departamento, e assim irá ter acesso aos treinamentos ofertados por aquele departamento.

Como forma de fomento a realização dos treinamentos, terá um ranking de conhecimento baseado na quantidade de cursos concluídos entre os integrantes de todos os departamentos.

### Tabela de Requisitos do Banco de Dados:
| #RBD  | Nome RBD                                            | Descrição RBD                                                                                                                                                |
| ----- | --------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| RBD01 | Armazenar as informações da organização             | Armazenar os atributos da organização que irá usar o sistema (cnpj, nome, tipo, quando foi criada, administrador que gerencia a organização, quantidade de funcionários.)                       |
| RBD02 | Armazenar as informações do administrador do sistema | Armazenar os atributos do administrador do sistema (código identificador, nome, cpf, data de nascimento, especialidade.)  |
| RBD03 | Armazenar os departamentos e seus atributos         | Armazenar cada departamento da organização (código do departamento, nome, sigla, gerente do departamento, contato (e-mail e telefone), quantidade de funcionários)                                                           |
| RBD04 | Armazenar os gerentes dos departamentos             | Armazenar os gerentes dos departamentos com sua designação (matrícula, nome, cpf, data de nascimento, especialidade)   
| RBD05 | Armazenar informações dos tutores            | Armazenar os dados dos tutores de cada departamento (código identificador, nome, cpf, cargo, departamento que ele está incluído, quantidade de novos integrantes que está responsável)                   |                                                                |
| RBD06 | Armazenar os cursos de cada departamento            | Armazenar os cursos de cada departamento (código do curso, nome, carga horária, departamento que ele está incluído, professor que leciona)                   |
| RBD07 | Armazenar os professores de cada curso              | Armazenar os professores de cada curso, associando qual curso que leciona (código professor, nome, cpf, data de nascimento, especialidade, códico do curso)                                                    |
| RBD08 | Armazenar os integrantes da instituição             | Armazenar os integrantes da organização, com sua associação com o departamento (matricula, nome, cpf, data de nascimento, e-mail, contato, cargo ou vínculo, departamento que ele está incluído, tutor, status da integração, data prevista para fim da integração)           |
| RBD09 | Armazenar o ranking de conhecimento                 | Armazenar o ranking de conhecimento dos integrantes (cpf do integrante, quantidade de cursos concluidos, posição no ranking, carga horária total de cursos estudados)                                 |
| RBD10 | Armazenar o progresso dos cursos dos integrantes    | Armazenar o progresso dos cursos feitos pelos integrantes (entidade fraca) (cpf do integrante, código do curso, progresso, concluído (True or False)) |
| RBD11 | Armazenar dados dos processos internos para consulta    | Catalogar os processos organizacionais (identificador, título, objetivo, passo a passo, público-alvo, prazo médio e data de atualização) e os documentos de apoio (manuais, normativas e formulários, tipo, link/conteúdo e data de publicação) |

### Regras de negócio:
- A Organização só pode ter 1 Administrador
- A Organização pode ter N Departamentos
- Somente o Administrador pode criar Departamentos
- O Administrador não pode criar cursos
- Cada um dos departamentos só pode ter 1 Gerente
- Cada Departamento pode ter N Integrantes
- Cada Departamento pode ter N Cursos
- Cada Curso pode ter somente 1 Professor
- Um Professor também é um Integrante
- Cada Integrante pode fazer N Cursos
- Cada Integrante tem que estar em somente 1 Departamento
- Cada tutor pode ter N integrantes
- cada integrante só pode ter um tutor


## MER (texto/tabela com entidades, atributos, chaves, relacionamentos, regras)



## DER (imagem legível, notação Chen ou Crow’s Foot)



## Esquema Relacional (tabelas, colunas, PK/FK, observações)



## Normalização (DFs + 1FN/2FN/3FN com justificativa)



## Amostra mínima de dados (5–10 tuplas relevantes) em formato de tabela



## 3–5 consultas em linguagem natural que o BD deve responder
