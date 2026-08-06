# 🎯 Objetivo
Esse projeto tem como objetivo planejar os cenários de acordo com os requisitos do sistema, executar os testes, documentar e registrar os bugs encontrados.

Para fins de estudos decidi escrever os casos de testes na liguagem Gherkin que é um dos elementos principais do BDD (Behavior Driven Development).

## O que são BDD e Gherkin

O BDD (Behavior Driven Development, ou Desenvolvimento Orientado ao Comportamento) é uma metodologia desenvolvimento orientada a comportamento, que busca alinhar as equipes técnicas e de negócios através de exemplos claros de como o sistema deve funcionar.
O principal objetivo é garantir que todos integrantes do time falem a mesma língua e tenham o mesmo entendimento de como o sistema deve funcionar, melhorando a comunicação e reduzindo erros.

Gherkin é a linguagem utilizada para descrever os comportamentos esperados do sistema. Sua função é padrozinar a escrita dos cenários de teste de forma simples e legível, podendo ser usado depois para realizar automação.

Principais palavras-chaves:
- Feature: Funcionalidade a ser testada
- Scenario: Cenário de teste
- Given(Dado) : Contexto inicial
- When(Quando) : Ação executada
- Then(Então) : Resultado esperado
- And(E): Complementa uma condição, ação ou resultado.

## Dados dos testes

**Data:** 05/08/2026
**Navegador:** Chrome
**Ambiente:** https://agendalabqa.vercel.app/login

Usuário: usuario_normal
Senha: secret123

## Requisitos da funcionalidade Novo Agendamento

![Requisitos da funcionalidade Novo Agendamento](/agendalab/funcionalidade-novo-agendamento/images/requisitos-novo-agendamento.png)

## 📋 Cenários

**Funcionalidade:** Novo Agendamento

### ✅ Cenário de sucesso (Caminho feliz)
**Cenário:** Realizar Novo Agendamento com sucesso

>**Dado** que usuário acessou a tela de Novo Agendamento\
**Quando** preenche os campos obrigatórios corretamente\
**E** clica no botão Confirmar Agendamento\
**Então** o agendamento deve ser criado com status “CONFIRMADO”\
**E** deve ser exibida a mensagem: “Agendamento Confirmado! Seu agendamento foi criado com sucesso e está com status CONFIRMADO.”

- **Status:** ✅ Aprovado
- **Evidência:** [001-agendamento-com-sucesso.gif](/agendalab/funcionalidade-novo-agendamento/images/001-agendamento-com-sucesso.gif)
- **Resultado obtido:** Agendamento realizado com sucesso.

### ❎ Cenários Alternativos e Negativos (Validações e Regras de Negócio)

**Cenário:** Tentar realizar Novo Agendamento com todos os campos obrigatórios vazios

>**Dado** que o usuário acessou a tela de Novo Agendamento\
**Quando** clica no botão “Confirmar Agendamento”\
**Então** deve exibir a mensagem “Nome do cliente é obrigatório.”\
**E** o agendamento não deve ser criado

- **Status:** ✅ Aprovado
- **Evidência:** [002-nome-obrigatorio](/agendalab/funcionalidade-novo-agendamento/images/002-nome-obrigatorio.png)
- **Resultado obtido:** Mensagem “Nome do cliente é obrigatório.” corretamente

**Cenário:** Tentativa de Novo Agendamento com o campo Nome vazio

>**Dado** que o usuário acessou a tela de Novo Agendamento\
**E** campo “Nome” está em branco\
**E** os demais campos obrigatórios estão preenchidos\
**Quando** clica no botão “Confirmar Agendamento”\
**Então** deve exibir a mensagem “Nome do cliente é obrigatório.”\
**E** o agendamento não deve ser criado

- **Status:** ✅ Aprovado
- **Evidência:** [003-nome-obrigatorio](/agendalab/funcionalidade-novo-agendamento/images/003-nome-obrigatorio.png)
- **Resultado obtido:** Mensagem “Nome do cliente é obrigatório.” exibida corretamente

**Cenário:** Tentar realizar um Novo Agendamento com o campo Telefone vazio

>**Dado** que o usuário acessou a tela de Novo Agendamento\
**E** campo “Telefone” está em branco\
**E** os demais campos obrigatórios estão preenchidos\
**Quando** clica no botão “Confirmar Agendamento”\
**Então** deve exibir a mensagem “Telefone é obrigatório.”\
**E** o agendamento não deve ser criado

- **Status:** ✅ Aprovado
- **Evidência:** [004-telefone-obrigatorio](/agendalab/funcionalidade-novo-agendamento/images/004-telefone-obrigatorio.png)
- **Resultado obtido:** Mensagem “Telefone é obrigatório.” exibida corretamente

**Cenário:** Tentar realizar um Novo Agendamento com o campo Serviço vazio

>**Dado** que o usuário acessou a tela de Novo Agendamento\
**E** campo “Serviço” não foi selecionado\
**E** os demais campos obrigatórios estão preenchidos\
**Quando** clica no botão “Confirmar Agendamento”\
**Então** deve exibir a mensagem “Serviço é obrigatório.”\
**E** o agendamento não deve ser criado

- **Status:** ✅ Aprovado
- **Evidência:** [005-servico-obrigatorio](/agendalab/funcionalidade-novo-agendamento/images/images/005-servico-obrigatorio.png)
- **Resultado obtido:** Mensagem “Serviço é obrigatório.” exibida corretamente

**Cenário:** Tentar realizar um Novo Agendamento com o campo Profissional vazio

>**Dado** que o usuário acessou a tela de Novo Agendamento\
**E** campo “Profissional” não foi selecionado\
**E** os demais campos obrigatórios estão preenchidos\
**Quando** clica no botão “Confirmar Agendamento”\
**Então** deve exibir a mensagem “Profissional é obrigatório.”\
**E** o agendamento não deve ser criado

- **Status:** ✅ Aprovado
- **Evidência:** [006-profissional-obrigatorio](/agendalab/funcionalidade-novo-agendamento/images/006-profissional-obrigatorio.png)
- **Resultado obtido:** Mensagem “Profissional é obrigatório.” exibida corretamente

**Cenário:** Tentar realizar Novo Agendamento com o campo Data vazio

>**Dado** que o usuário acessou a tela de Novo Agendamento\
**E** campo “Data” está em branco\
**E** os demais campos obrigatórios estão preenchidos\
**Quando** clica no botão “Confirmar Agendamento”\
**Então** deve exibir a mensagem “Data é obrigatória.”\
**E** o agendamento não deve ser criado

- **Status:** ✅ Aprovado
- **Evidência:** [007-data-obrigatoria](/agendalab/funcionalidade-novo-agendamento/images/007-data-obrigatoria.png)
- **Resultado obtido:** Mensagem “Data é obrigatória.” exibida corretamente

**Cenário:** Tentar realizar Novo Agendamento com o campo Horário vazio

>**Dado** que o usuário acessou a tela de Novo Agendamento\
**E** campo “Horário” está em branco\
**E** os demais campos obrigatórios estão preenchidos\
**Quando** clica no botão “Confirmar Agendamento”\
**Então** deve exibir a mensagem “Horário é obrigatório.”\
**E** o agendamento não deve ser criado

- **Status:** ✅ Aprovado
- **Evidência:** [008-horario-obrigatorio](/agendalab/funcionalidade-novo-agendamento/images/008-horario-obrigatorio.png)
- **Resultado obtido:** Mensagem “Horário é obrigatório.” exibida corretamente

#### 👤 Validações do campo Nome

**Cenário:** Tentar realizar Novo Agendamento preenchendo o campo Nome somente com números

>**Dado** que o usuário acessou a tela de Novo Agendamento\
**E** campo “Nome” está preenchido com “123”\
**E** os demais campos obrigatórios estão preenchidos\
**Quando** clica no botão “Confirmar Agendamento”\
**Então** deve exibir a mensagem “Nome preenchido de forma incorreta”\
**E** o agendamento não deve ser criado

- **Status:** ❌ Reprovado
- **Evidência:** [009-nome](/agendalab/funcionalidade-novo-agendamento/images/009-nome.gif)
- **Resultado obtido:** Não foi exibida a mensagem mensagem “Nome do cliente é obrigatório.” e cadastrou o novo agendamento.

**Cenário:** Tentar realizar Novo Agendamento preenchendo o campo Nome somente com espaços

>**Dado** que o usuário acessou a tela de Novo Agendamento\
**E** campo “Nome” está preenchido com “   ”\
**E** os demais campos obrigatórios estão preenchidos\
**Quando** clica no botão “Confirmar Agendamento”\
**Então** deve exibir a mensagem “Nome do cliente é obrigatório.”\
**E** o agendamento não deve ser criado

- **Status:** ✅ Aprovado
- **Evidência:** [010-nome](/agendalab/funcionalidade-novo-agendamento/images/010-nome.gif)
- **Resultado obtido:** Foi exibida a mensagem “Nome do cliente é obrigatório.”.


#### 📞 Validações do Campo Telefone

**Cenário:** Tentar realizar Novo Agendamento preenchendo o campo telefone com apenas 5 dígitos

>**Dado** que o usuário acessou a tela de Novo Agendamento\
**E** campo “Telefone” está preenchido com “12345”\
**E** os demais campos obrigatórios estão preenchidos\
**Quando** clica no botão “Confirmar Agendamento”\
**Então** deve exibir a mensagem “Formato do telefone incorreto”\
**E** o agendamento não deve ser criado

- **Status:** ❌ Reprovado
- **Evidência:** [011-telefone](/agendalab/funcionalidade-novo-agendamento/images/011-telefone.gif)
- **Resultado obtido:** Não foi exibida a mensagem mensagem “Formato do telefone incorreto”, cadastrou o novo agendamento com sucesso.

**Cenário:** Tentar realizar Novo Agendamento preenchendo o campo telefone apenas com espaços em branco

>**Dado** que o usuário acessou a tela de Novo Agendamento\
**E** campo “Telefone” está preenchido com “   ”\
**E** os demais campos obrigatórios estão preenchidos\
**Quando** clica no botão “Confirmar Agendamento”\
**Então** deve exibir a mensagem “Telefone é obrigatório.”\
**E** o agendamento não deve ser criado

- **Status:** ✅ Aprovado
- **Evidência:** [012-telefone](/agendalab/funcionalidade-novo-agendamento/images/012-telefone.gif)
- **Resultado obtido:** Ao preencher o campo telefone com apenas espaços e tentar realizar um novo agendamento a mensagem “Telefone é obrigatório.” é exibida corretamente.

**Cenário:** Tentar um Novo Agendamento preenchendo o campo telefone apenas com um caractere

>**Dado** que o usuário acessou a tela de Novo Agendamento\
**E** campo “Telefone” está preenchido com “-”\
**E** os demais campos obrigatórios estão preenchidos\
**Quando** clica no botão “Confirmar Agendamento”\
**Então** deve exibir a mensagem “Formato do telefone incorreto”\
**E** o agendamento não deve ser criado

- **Status:** ❌ Reprovado
- **Evidência:** [013-telefone](/agendalab/funcionalidade-novo-agendamento/images/013-telefone.gif)
- **Resultado obtido:** Ao preencher o campo telefone com um hífen e tentar realizar um novo agendamento não é exibida nenhuma mensagem de erro e o novo agendamento é cadastrado com sucesso.

**Cenário:** Tentar um Novo Agendamento preenchendo o campo telefone com parenteses no meio dos números

>**Dado** que o usuário acessou a tela de Novo Agendamento\
**E** campo “Telefone” está preenchido com “(11) 9123)567(”\
**E** os demais campos obrigatórios estão preenchidos\
**Quando** clica no botão “Confirmar Agendamento”\
**Então** deve exibir a mensagem “Formato do telefone incorreto”\
**E** o agendamento não deve ser criado

- **Status:** ❌ Reprovado
- **Evidência:** [014-telefone](/agendalab/funcionalidade-novo-agendamento/images/014-telefone.gif)
- **Resultado obtido:** Ao preencher o campo telefone com “(11) 9123)567(” não foi exibida a mensagem “Formato do telefone incorreto” e o agendamento foi cadastrado com sucesso. 

**Cenário:** Tentar um Novo Agendamento preenchendo o campo telefone contendo números e letras

>**Dado** que o usuário acessou a tela de Novo Agendamento\
**E** campo “Telefone” está preenchido com “912345678abc”\
**E** os demais campos obrigatórios estão preenchidos\
**Quando** clica no botão “Confirmar Agendamento”\
**Então** deve exibir a mensagem “Telefone inválido. Use apenas números, parênteses, espaços e hífens.”\
**E** o agendamento não deve ser criado

- **Status:** ✅ Aprovado
- **Evidência:** [015-telefone](/agendalab/funcionalidade-novo-agendamento/images/015-telefone.gif)
- **Resultado obtido:** Ao preencher o campo telefone com “912345678abc” foi exibida corretamente a mensagem “Telefone inválido. Use apenas números, parênteses, espaços e hífens.”

**Cenário:** Tentar um Novo Agendamento preenchendo o campo telefone contendo caractere especial

>**Dado** que o usuário acessou a tela de Novo Agendamento\
**E** campo “Telefone” está preenchido com “(11) 91234-567#”\
**E** os demais campos obrigatórios estão preenchidos\
**Quando** clica no botão “Confirmar Agendamento”\
**Então** deve exibir a mensagem “Telefone inválido. Use apenas números, parênteses, espaços e hífens.”\
**E** o agendamento não deve ser criado

- **Status:** ✅ Aprovado
- **Evidência:** [016-telefone](/agendalab/funcionalidade-novo-agendamento/images/016-telefone.gif)
- **Resultado obtido:** Ao preencher o campo telefone com “(11) 91234-567#” foi exibida corretamente a mensagem “Telefone inválido. Use apenas números, parênteses, espaços e hífens.”

#### 📝 Validações do Campo Observações

**Cenário:** Tentar um Novo Agendamento preenchendo o campo Observações com 200 caracteres

>**Dado** que o usuário acessou a tela de Novo Agendamento\
**E** campo “Observação” é preenchido com 200 caracteres \
**E** os demais campos obrigatórios estão preenchidos\
**Quando** clica no botão “Confirmar Agendamento”\
**Então** o agendamento deve ser criado com status “CONFIRMADO”\
**E** deve ser exibida a mensagem “Agendamento Confirmado! ****Seu agendamento foi criado com sucesso e está com status CONFIRMADO.”

- **Status:** ✅ Aprovado
- **Evidência:** [017-observacoes](/agendalab/funcionalidade-novo-agendamento/images/017-observacoes.gif)
- **Resultado obtido:** Ao preencher o campo Observações com um texto com 200 caracteres incluindo os espaços, o agendamento foi realizado com sucesso.

**Cenário:** Tentar um Novo Agendamento preenchendo o campo Observações com mais de 200 caracteres

>**Dado** que o usuário acessou a tela de Novo Agendamento\
**E** campo “Observação” é preenchido com mais 200 caracteres \
**E** os demais campos obrigatórios estão preenchidos\
**Quando** clica no botão “Confirmar Agendamento”\
**Então** deve exibir a mensagem “Observação com mais de 200 caracteres”

- **Status:** ✅ Aprovado
- **Evidência:** [018-observacoes](/agendalab/funcionalidade-novo-agendamento/images/018-observacoes.gif)
- **Resultado obtido:** Ao tentar inserir uma observação com mais de 200 caracteres o campo limitou a quantidade para 200 caracteres e ignorou o restante do texto.

#### 🗓️ Validações de Data (Passado e Domingo)

**Cenário:** Tentar um Novo Agendamento preenchendo o campo Data com uma data passada

>**Dado** que o usuário acessou a tela de Novo Agendamento\
**E** campo “Data” é preenchido com uma data passada\
**E** os demais campos obrigatórios estão preenchidos\
**Quando** clica no botão “Confirmar Agendamento”\
**Então** deve exibir a mensagem “Não é possível agendar para uma data passada.”

- **Status:** ✅ Aprovado
- **Evidência:** [019-data-passada](/agendalab/funcionalidade-novo-agendamento/images/019-data-passada-ou-domingo.gif)
- **Resultado obtido:** Ao tentar selecionar uma data passada foi exibida corretamente a mensagem “Não é possível agendar para uma data passada.”

**Cenário:** Tentar um Novo Agendamento para um domingo

>**Dado** que o usuário acessou a tela de Novo Agendamento\
**Quando** campo “Data” é preenchido com “09/08/2026” (Domingo)\
**Então** deve exibir a mensagem “Domingos não são permitidos para agendamento.”

- **Status:** ✅ Aprovado
- **Evidência:** [020-data-domingo](/agendalab/funcionalidade-novo-agendamento/images/020-data-passada-ou-domingo.gif)
- **Resultado obtido:** Ao tentar selecionar uma data passada foi exibida corretamente a mensagem “Domingos não são permitidos para agendamento.”

#### 🕒 Validações do Horário

**Cenário:** Tentar um Novo Agendamento selecionando um horário fora da grade permitida

>**Dado** que o usuário acessou a tela de Novo Agendamento\
**E** a lista de horários disponíveis exibe apenas: 08h, 09h, 10h, 11h, 13h, 14h, 15h, 16h, 17h\
**Quando** o usuário tenta inserir ou selecionar um horário inválido, por exemplo: 07h, 12h ou 18h\
**Então** o sistema não deve permitir a seleção do horário inválido

- **Status:** ✅ Aprovado
- **Evidência:** [021-horário-fora-da-grade-permitida](/agendalab/funcionalidade-novo-agendamento/images/021-horario-fora-da-grade-permitida.gif)
- **Resultado obtido:** O sistema não permitiu selecionar ou inserir um um horário fora da grade permitida.

**Cenário:** Tentar um Novo Agendamento com data e horário e para o mesmo profissional (mesmo profissional + data + horário CONFIRMADO)

>**Dado** que já existe um agendamento com o profissional “Dra. Ana Souza” para o dia “10/08/2026” às “10h” com status CONFIRMADO\
**E** na tela de Novo Agendamento o usuário preenche o campo “Nome”, “Telefone” e “Serviço”\
**E** seleciona a mesma profissional “Dra. Ana Souza”\
**E** seleciona a mesma data “18/08/2026”\
**Quando** o usuário tenta selecionar o horário “10:00”\
**Então** o horário deve aparecer da seguinte forma “10:00 - indisponível” e bloqueado para seleção.

- **Status:** ✅ Aprovado
- **Evidência:** [022-data-horario-profissional-conflito](/agendalab/funcionalidade-novo-agendamento/images/022-data-hora-profissonal-conflito.gif)
- **Resultado obtido:** O sistema não permitiu criar um novo agendamento com o mesmo profissional, data e horário de um agendamento já confirmado.

## 🐞 Bug Report (Em construção 🚧)
