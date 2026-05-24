README - QA, TESTES MANUAIS E TESTES AUTOMATICOS - MEDSAVE
============================================================

Projeto: MedSave
Area da entrega: QA - Qualidade de Software
Tema: Testes manuais e testes automaticos da API MedSave


1. VISAO GERAL DO PROJETO
-------------------------

O MedSave e uma solucao tecnologica desenvolvida para auxiliar na gestao de medicamentos em ambientes de saude, como hospitais, UBSs, UPAs e farmacias publicas.

A proposta do sistema e melhorar o controle, a seguranca e a rastreabilidade dos medicamentos, reduzindo problemas como desperdicio, falta de controle de estoque, falhas em movimentacoes e dificuldade de acompanhamento das informacoes.

Dentro da parte de Qualidade de Software, foram planejadas e executadas atividades de testes com o objetivo de validar o funcionamento da API do MedSave. Como o projeto nao possui uma interface web tradicional, os testes foram direcionados principalmente para a camada de API REST.

Os testes foram divididos em duas partes principais:

- Testes manuais, planejados no Azure Boards e executados com apoio do Insomnia.
- Testes automaticos, executados por meio de colecoes e validacoes automatizadas, com foco nos principais endpoints da API.


2. OBJETIVO DA PARTE DE QA
--------------------------

A parte de QA do projeto MedSave tem como objetivo garantir que as funcionalidades principais da API estejam funcionando corretamente, tanto em cenarios de sucesso quanto em cenarios de erro.

Com os testes, buscamos verificar se a API:

- Realiza login corretamente.
- Retorna token JWT em autenticacoes validas.
- Protege endpoints que exigem autenticacao.
- Permite cadastrar medicamentos com dados validos.
- Permite listar medicamentos cadastrados.
- Permite buscar medicamentos por ID.
- Permite atualizar medicamentos existentes.
- Permite excluir medicamentos existentes.
- Retorna erros adequados quando os dados enviados sao invalidos.
- Impede operacoes indevidas, como acesso sem token ou busca de registros inexistentes.

Essas validacoes ajudam a comprovar que o sistema esta se comportando conforme o esperado e que os principais fluxos da API foram testados.


3. PARTE A - TESTES MANUAIS
---------------------------

A Parte A da atividade teve como foco a criacao de um plano de testes manuais em nivel de sistema.

Como o MedSave nao possui uma interface web, os testes manuais foram planejados para a camada de API REST. Isso significa que, em vez de testar botoes ou telas web, os testes validam diretamente os endpoints da API.

Para isso, foram utilizados:

- Azure Boards: para organizar e documentar o planejamento dos testes.
- Insomnia: para executar manualmente as requisicoes HTTP.


4. FERRAMENTAS UTILIZADAS
-------------------------

4.1 Azure Boards
~~~~~~~~~~~~~~~~

O Azure Boards foi utilizado para organizar as atividades de teste, conforme solicitado na atividade.

Nele foram registrados os itens de planejamento, seguindo uma estrutura hierarquica com Epic, Feature, Product Backlog Item e Tasks.

A organizacao no Azure Boards ajuda a demonstrar que os testes foram planejados antes da execucao e que existe uma estrutura formal para acompanhar as atividades de QA.


4.2 Insomnia
~~~~~~~~~~~~

O Insomnia foi utilizado para executar manualmente as requisicoes da API.

Com ele, foi possivel validar:

- Metodo HTTP utilizado.
- URL do endpoint.
- Corpo JSON enviado.
- Headers da requisicao.
- Token JWT de autenticacao.
- Status code retornado.
- Corpo JSON da resposta.
- Mensagens de erro.

O Insomnia foi escolhido porque permite testar APIs REST de forma simples, organizada e visual.


4.3 API REST MedSave
~~~~~~~~~~~~~~~~~~~~

A API REST do MedSave foi o principal objeto de teste.

Os endpoints testados envolvem principalmente:

- Autenticacao de usuarios.
- CRUD de medicamentos.

CRUD significa:

- Create: cadastro/criacao de registros.
- Read: leitura/listagem/busca de registros.
- Update: atualizacao de registros.
- Delete: exclusao de registros.


5. ORGANIZACAO DOS TESTES NO AZURE BOARDS
-----------------------------------------

As atividades de teste foram organizadas no Azure Boards seguindo a estrutura abaixo:

EPIC:
- Validacao e testes da API MedSave

FEATURE:
- Planejamento de testes manuais da API

PRODUCT BACKLOG ITEM:
- Criar plano de testes manuais dos endpoints da API MedSave

TASKS:
- Casos de teste manuais, como login, cadastro, listagem, busca, atualizacao e exclusao de medicamentos.

Essa estrutura permite demonstrar que o planejamento foi feito de forma organizada, separando a entrega principal em atividades menores e mais controladas.


6. CASOS DE TESTE MANUAIS PLANEJADOS
------------------------------------

Os testes manuais foram organizados como CTM, que significa Caso de Teste Manual.

Foram planejados os seguintes casos de teste:

CTM01 - Login com credenciais validas
Objetivo: verificar se a API permite autenticar um usuario valido e retorna um token JWT.

CTM02 - Cadastro de medicamento com dados validos
Objetivo: verificar se a API permite cadastrar um novo medicamento quando todos os dados obrigatorios sao enviados corretamente.

CTM03 - Listagem de medicamentos cadastrados
Objetivo: verificar se a API retorna a lista de medicamentos ja cadastrados no sistema.

CTM04 - Busca de medicamento por ID
Objetivo: verificar se a API retorna corretamente os dados de um medicamento existente a partir do seu ID.

CTM05 - Atualizacao de medicamento existente
Objetivo: verificar se a API permite atualizar os dados de um medicamento ja cadastrado.

CTM06 - Exclusao de medicamento existente
Objetivo: verificar se a API permite excluir um medicamento existente.

CTM07 - Login com credenciais invalidas
Objetivo: verificar se a API bloqueia a autenticacao quando email ou senha estao incorretos.

CTM08 - Cadastro de medicamento duplicado
Objetivo: verificar se a API impede o cadastro duplicado de um medicamento, por exemplo, com o mesmo codigo ANVISA ou outro campo unico.

CTM09 - Listagem de medicamentos sem token
Objetivo: verificar se a API bloqueia o acesso a endpoints protegidos quando o token JWT nao e enviado.

CTM10 - Busca de medicamento inexistente
Objetivo: verificar se a API retorna erro adequado ao buscar um medicamento com ID inexistente.

CTM11 - Atualizacao de medicamento inexistente
Objetivo: verificar se a API retorna erro ao tentar atualizar um medicamento que nao existe.

CTM12 - Exclusao de medicamento inexistente
Objetivo: verificar se a API retorna erro ao tentar excluir um medicamento que nao existe.


7. ITENS OBRIGATORIOS ATENDIDOS NOS TESTES MANUAIS
--------------------------------------------------

Para cada caso de teste manual, foram descritos os itens solicitados na atividade:

1. Testes planejados
2. Dados de entrada
3. Dados de saida esperados
4. Procedimento de teste


7.1 Testes planejados
~~~~~~~~~~~~~~~~~~~~~

Cada teste foi identificado por um codigo CTM e por um nome descritivo.

Exemplo:

CTM01 - Login com credenciais validas

Esse padrao facilita a identificacao dos testes dentro do Azure Boards e tambem facilita a apresentacao para o professor.


7.2 Dados de entrada
~~~~~~~~~~~~~~~~~~~~

Os dados de entrada representam tudo que e necessario informar para executar o teste.

Foram considerados como dados de entrada:

- Endpoint da API.
- Metodo HTTP.
- Corpo JSON da requisicao.
- Token JWT, quando necessario.
- ID de medicamento existente ou inexistente.
- Parametros enviados pela URL.

Exemplo de dado de entrada para login:

Endpoint:
/api/v4/auth/login

Metodo HTTP:
POST

Body JSON:
{
  "email": "prof@fiap.com.br",
  "password": "12345678"
}


7.3 Dados de saida esperados
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Os dados de saida esperados indicam qual deve ser o resultado correto depois da execucao do teste.

Foram considerados como saidas esperadas:

- Status code HTTP.
- Corpo JSON de resposta.
- Presenca de token JWT.
- ID gerado no cadastro.
- Mensagem de erro em cenarios invalidos.
- Confirmacao de atualizacao ou exclusao.

Exemplo de saida esperada para login valido:

Status code esperado:
200 OK

Retorno esperado:
JSON contendo um token JWT.


7.4 Procedimento de teste
~~~~~~~~~~~~~~~~~~~~~~~~~

O procedimento de teste descreve o passo a passo para executar cada caso manualmente.

Exemplo de procedimento para login valido:

1. Abrir o Insomnia.
2. Selecionar a requisicao de login.
3. Informar o endpoint /api/v4/auth/login.
4. Selecionar o metodo POST.
5. Inserir o JSON com email e senha validos.
6. Enviar a requisicao.
7. Verificar se o status code retornado e 200.
8. Verificar se a resposta contem um token JWT.
9. Registrar o resultado do teste.


8. CENARIOS DE SUCESSO
----------------------

Os cenarios de sucesso validam o funcionamento correto da API quando os dados enviados sao validos.

Foram considerados cenarios como:

- Login com usuario valido.
- Cadastro de medicamento com dados obrigatorios preenchidos.
- Listagem de medicamentos cadastrados.
- Busca de medicamento existente por ID.
- Atualizacao de medicamento existente.
- Exclusao de medicamento existente.

Esses testes comprovam que os fluxos principais do sistema funcionam corretamente quando o usuario utiliza a API da forma esperada.


9. CENARIOS DE ERRO
-------------------

Tambem foram planejados cenarios negativos para validar o comportamento da API diante de entradas invalidas ou operacoes incorretas.

Foram considerados cenarios como:

- Login com credenciais invalidas.
- Cadastro de medicamento duplicado.
- Listagem de medicamentos sem token JWT.
- Busca de medicamento com ID inexistente.
- Atualizacao de medicamento inexistente.
- Exclusao de medicamento inexistente.

Esses testes sao importantes porque mostram que a API nao deve apenas funcionar em situacoes corretas, mas tambem deve tratar erros de forma adequada.


10. PARTE B - TESTES AUTOMATICOS
--------------------------------

A Parte B da atividade esta relacionada aos testes automaticos da API MedSave.

Os testes automaticos servem para validar os endpoints de forma mais rapida e repetivel, sem depender da execucao manual de cada requisicao.

No contexto do MedSave, os testes automaticos foram utilizados para verificar se os principais endpoints da API continuam respondendo corretamente depois de alteracoes no codigo.

A principal vantagem dos testes automaticos e que eles podem ser executados varias vezes com os mesmos dados controlados, ajudando a encontrar erros com mais facilidade.


11. OBJETIVO DOS TESTES AUTOMATICOS
-----------------------------------

Os testes automaticos tem como objetivo validar os principais comportamentos da API de forma padronizada.

Eles ajudam a verificar:

- Se o endpoint esta disponivel.
- Se o metodo HTTP correto esta sendo utilizado.
- Se o status code retornado esta correto.
- Se o corpo da resposta possui os campos esperados.
- Se o token JWT e retornado corretamente no login.
- Se a API bloqueia acessos sem autenticacao.
- Se os cadastros, buscas, atualizacoes e exclusoes funcionam corretamente.


12. RELACAO ENTRE TESTES MANUAIS E AUTOMATICOS
----------------------------------------------

Os testes manuais e automaticos se complementam.

Os testes manuais foram importantes para planejar, documentar e validar passo a passo os principais fluxos da API.

Ja os testes automaticos foram importantes para repetir essas validacoes de maneira mais rapida, reduzindo o trabalho manual e ajudando a identificar possiveis falhas apos alteracoes no sistema.

De forma simples:

- Teste manual: bom para documentar, analisar e validar o comportamento com mais detalhe.
- Teste automatico: bom para repetir validacoes rapidamente e garantir estabilidade da API.


13. EXEMPLOS DE VALIDACOES AUTOMATICAS
--------------------------------------

Algumas validacoes que podem ser feitas automaticamente:

Teste de login valido:
- Enviar email e senha validos.
- Esperar status code 200.
- Verificar se existe token JWT na resposta.

Teste de login invalido:
- Enviar email ou senha incorretos.
- Esperar status code de erro.
- Verificar se a API nao retorna token.

Teste de listagem de medicamentos:
- Enviar requisicao GET para o endpoint de medicamentos.
- Informar token JWT no header Authorization.
- Esperar status code 200.
- Verificar se o retorno esta em formato JSON.

Teste de acesso sem token:
- Enviar requisicao para endpoint protegido sem Authorization.
- Esperar status code 401 Unauthorized ou 403 Forbidden, conforme configuracao da API.

Teste de busca por ID inexistente:
- Enviar requisicao GET com um ID que nao existe.
- Esperar status code 404 Not Found ou mensagem de erro adequada.


14. PRINCIPAIS ENDPOINTS CONSIDERADOS
-------------------------------------

Os endpoints podem variar conforme a versao da API, mas a estrutura considerada nos testes foi semelhante a esta:

Autenticacao:
POST /api/v4/auth/login

Medicamentos:
POST /api/v4/medicines
GET /api/v4/medicines
GET /api/v4/medicines/{id}
PUT /api/v4/medicines/{id}
DELETE /api/v4/medicines/{id}

Observacao:
Os endpoints devem ser ajustados conforme a versao final da API utilizada na entrega.


15. EXEMPLO DE TESTE MANUAL DOCUMENTADO
---------------------------------------

Codigo do teste:
CTM01

Nome:
Login com credenciais validas

Objetivo:
Validar se um usuario cadastrado consegue realizar login corretamente na API MedSave.

Dados de entrada:

Endpoint:
/api/v4/auth/login

Metodo:
POST

Body:
{
  "email": "prof@fiap.com.br",
  "password": "12345678"
}

Dados de saida esperados:

- Status code 200 OK.
- Retorno em JSON.
- Presenca de token JWT na resposta.

Procedimento:

1. Abrir o Insomnia.
2. Criar ou selecionar a requisicao de login.
3. Informar o metodo POST.
4. Informar a URL da API com o endpoint /api/v4/auth/login.
5. Inserir o body JSON com email e senha validos.
6. Enviar a requisicao.
7. Conferir se o status code retornado e 200.
8. Conferir se o retorno possui token JWT.
9. Registrar o resultado no plano de testes.

Resultado esperado:
Login realizado com sucesso e token retornado pela API.


16. EXEMPLO DE TESTE DE ERRO DOCUMENTADO
----------------------------------------

Codigo do teste:
CTM07

Nome:
Login com credenciais invalidas

Objetivo:
Validar se a API bloqueia login quando o usuario informa credenciais incorretas.

Dados de entrada:

Endpoint:
/api/v4/auth/login

Metodo:
POST

Body:
{
  "email": "usuario_invalido@fiap.com.br",
  "password": "senhaerrada"
}

Dados de saida esperados:

- Status code de erro, como 401 Unauthorized ou 403 Forbidden, conforme configuracao da API.
- A API nao deve retornar token JWT.
- A API deve retornar uma mensagem de erro ou resposta indicando falha na autenticacao.

Procedimento:

1. Abrir o Insomnia.
2. Selecionar a requisicao de login.
3. Informar o metodo POST.
4. Inserir email ou senha invalidos no body JSON.
5. Enviar a requisicao.
6. Verificar se o status code indica erro.
7. Verificar se a resposta nao contem token JWT.
8. Registrar o resultado no plano de testes.

Resultado esperado:
A API deve impedir o login e nao deve gerar token.


17. BOAS PRATICAS APLICADAS
---------------------------

Durante o planejamento dos testes, foram aplicadas algumas boas praticas de QA:

- Separacao entre cenarios positivos e negativos.
- Uso de dados controlados.
- Identificacao dos testes por codigo.
- Descricao clara dos dados de entrada.
- Definicao dos resultados esperados.
- Criacao de passo a passo para execucao manual.
- Organizacao das atividades no Azure Boards.
- Validacao dos endpoints principais da API.
- Uso do Insomnia para simular chamadas reais HTTP.



