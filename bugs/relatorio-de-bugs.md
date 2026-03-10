# Relatório de Bugs

Este documento descreve os principais problemas identificados durante os testes no módulo de cadastro e listagem de cursos.

---

## BUG 01 — Sistema permite cadastrar curso com formulário vazio

**Severidade:** Alta  

**Descrição:**  
O sistema permite cadastrar um curso mesmo quando nenhum campo do formulário é preenchido.

**Passos para reproduzir:**

1. Acessar a aplicação.
2. Clicar em **Cadastrar curso**.
3. Não preencher nenhum campo do formulário.
4. Clicar no botão **Cadastrar curso**.

**Resultado atual:**  
O sistema permite o cadastro e exibe mensagem informando sucesso.

**Resultado esperado:**  
O sistema deveria impedir o cadastro e informar que os campos obrigatórios precisam ser preenchidos.

**Impacto:**  
Permite salvar registros inválidos, comprometendo a integridade dos dados.

---

## BUG 02 — Falta de validação para dados inválidos no formulário

**Severidade:** Alta  

**Descrição:**  
O sistema permite cadastrar cursos com dados inconsistentes, como número de vagas negativo ou data de término anterior à data de início.

**Passos para reproduzir:**

1. Acessar **Cadastrar curso**.
2. Preencher o formulário com:
   - Número de vagas negativo ou
   - Data de fim anterior à data de início.
3. Clicar em **Cadastrar curso**.

**Resultado atual:**  
O sistema aceita os dados e exibe mensagem de sucesso.

**Resultado esperado:**  
O sistema deveria validar os campos e impedir o cadastro com dados inválidos.

**Impacto:**  
Pode gerar registros inconsistentes e comprometer a confiabilidade das informações cadastradas.

---

## BUG 03 — Exclusão de curso não remove o registro da listagem

**Severidade:** Alta  

**Descrição:**  
Ao tentar excluir um curso, o sistema exibe mensagem de sucesso, porém o curso permanece visível na listagem.

**Passos para reproduzir:**

1. Acessar **Listar cursos**.
2. Localizar um curso existente.
3. Clicar em **Excluir curso**.
4. Atualizar a página.

**Resultado atual:**  
A mensagem informa sucesso na exclusão, mas o curso continua exibido.

**Resultado esperado:**  
O curso deveria ser removido da listagem após a exclusão.

**Impacto:**  
Gera inconsistência entre a ação executada e o feedback apresentado ao usuário.

---

## BUG 04 — Listagem apresenta problemas de organização ao exibir vários cursos

**Severidade:** Média  

**Descrição:**  
Ao cadastrar vários cursos, a listagem apresenta problemas de organização visual, afetando o alinhamento e a leitura das informações.

**Passos para reproduzir:**

1. Cadastrar múltiplos cursos na aplicação.
2. Acessar a tela **Listar cursos**.
3. Observar a disposição dos cards na interface.

**Resultado atual:**  
Os cards ficam desorganizados visualmente, dificultando a leitura das informações.

**Resultado esperado:**  
A listagem deveria manter organização visual consistente independentemente da quantidade de cursos cadastrados.

**Impacto:**  
Prejudica a experiência do usuário e dificulta a navegação.
