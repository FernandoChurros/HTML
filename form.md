
 # Formulário

 `<form>`
  - definirá o formulário, é um container estilo `<footer>` e `<header>`
 ## Atributos
  - action
    - Para onde o formulário será submetido.
  - method
    - GET e POST.
---
 
 # Fieldset e Legend

 ## `<fieldset>`
  - agrupamento de campos
  - mesmo propósito
  - semântico
  - acessibilidade

 ### Atributos especiais
  - Disabled
    - Desabilita todos os elementos internos
    - Não serão enviados ao submeter o formulário

  - form
    - O id de um formulário ao qual esse fieldset pertence
    - não precisa estar dentro do formulário

  - name
    - Nome do grupo

 ## `<legend>`
  - Nome do agrupamento
  - Primeiro elementos dentro do field set
---

 # Label

 ## `<label>`
  - Associar e identificar uma (ou mais) tag de entrade de dados
  - acessibilidade
  - você poderá clicar para mudar o foco da entrada de dados

 ### Atributos
  - for
    - Para fazer a conexão entre este label e a ta de entrada de dados
    - É feita via id do input
    - Só funciona com elementos específicos
    - buton, input (not hidden), meter, output, progress, select, textarea
---

 # Button

 ## `<button>`
  - Representa um botão
  - Usado para enviar formulários
  - É estilizado pelo user agent

 ### Atributos
  - type
    - submit
    - reset
    - button
  - autofocus
  - disabled
  - name
  - value
  - form
---

 # Datalist

 ## `<datalist>`
  - Lista de valores c omo sugestão a uma tag <input>
  - Valores sugestivos e não obrigatórios
  - Usuários poderão selecionar um dos valores, ou colocar um valor diferente da sugestão

 ```
  <input type="text" list="fruitsdata">
	<datalist id="fruitsdata">
	   <option>apple</option>
	   <option>orange</option>
	   <option>mango</option>
	   <option>cherry</option>
	</datalist>
 ```

 ## List 
  - Recebe como valor o id de um `<datalist>` residente no mesmo documento

 ## Tipos de inputs suportados
  - text, search, url, tel, email, date, month, week, time, datetime-local, number, range e color
