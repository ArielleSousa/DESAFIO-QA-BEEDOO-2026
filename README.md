# DESAFIO-QA-BEEDOO-2026

## Análise inicial da aplicação

A aplicação analisada tem como objetivo permitir o cadastro e a listagem de cursos.  
O sistema apresenta dois fluxos principais: visualização da lista de cursos cadastrados e cadastro de novos cursos.

Ao acessar a aplicação pela primeira vez, a tela inicial apresenta a seção "Lista de cursos". No entanto, quando não existem cursos cadastrados, não há nenhuma mensagem indicando esse estado ao usuário. Isso pode gerar confusão, pois não fica claro se não existem cursos cadastrados ou se ocorreu algum erro no carregamento.

Durante a exploração inicial, foi possível identificar que a navegação principal da aplicação é composta por dois itens:

- Listar cursos
- Cadastrar curso

A tela inicial corresponde à listagem de cursos cadastrados.

---

## Fluxos principais disponíveis

Os fluxos principais identificados na aplicação são:

- Acessar a listagem de cursos
- Acessar o formulário de cadastro de curso
- Preencher e enviar o formulário de cadastro
- Visualizar cursos cadastrados na listagem
- Excluir cursos cadastrados

---

## Campos identificados no cadastro de curso

Durante a análise da tela de cadastro, foram identificados os seguintes campos:

- Nome do curso
- Descrição do curso
- Instrutor
- URL da imagem de capa
- Data de início
- Data de fim
- Número de vagas
- Tipo de curso

Além desses campos, o sistema apresenta campos condicionais dependendo do tipo de curso selecionado:

Curso presencial:
- Endereço

Curso online:
- Link de inscrição

---

## Pontos críticos para teste

Durante a análise da aplicação, foram identificados alguns pontos críticos que devem ser priorizados durante os testes:

- Validação dos campos obrigatórios
- Comportamento do sistema ao enviar formulários incompletos
- Regras de preenchimento das datas (data de início e data de fim)
- Validação do campo número de vagas
- Regras relacionadas ao campo tipo de curso
- Comportamento dos campos condicionais (endereço e link de inscrição)
- Consistência da listagem após cadastro
- Exibição correta das informações cadastradas
- Exclusão de cursos cadastrados

---

## Decisões tomadas para criação dos testes

Os cenários de teste foram definidos com foco em cobrir os principais fluxos da aplicação, priorizando:

- fluxo principal de cadastro de curso
- validação dos campos do formulário
- cenários negativos
- comportamento da listagem após cadastro
- consistência das informações exibidas

A estratégia adotada foi priorizar qualidade da análise e cobertura dos cenários críticos da aplicação.

---

## Raciocínio durante a análise

A análise inicial foi realizada por meio de testes exploratórios na aplicação, buscando compreender o comportamento do sistema e identificar possíveis falhas.

Durante esses testes foram executados cenários positivos e negativos, incluindo tentativas de cadastro com campos vazios, valores inválidos e combinações inconsistentes de dados.

Esses testes permitiram identificar falhas importantes relacionadas principalmente à ausência de validação de campos obrigatórios e à aceitação de dados inconsistentes no cadastro de cursos.

---

## Casos de teste

Link da planilha contendo cenários e casos de teste:

(em breve)

---

## Evidências de execução

As evidências da execução dos testes estão disponíveis na pasta de evidências.

(em breve)

---

## Bugs encontrados

Os bugs identificados durante os testes estão documentados no arquivo:

/bugs/relatorio-de-bugs.md
