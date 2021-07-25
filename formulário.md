
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
---

 # Tags de entrada de dados
 
 ## `<input>`
  - Um dos mais usados um formulários
  - Aceita os mais diversos tipos de dados
  - Elevado números de combinações

 ### Atributos
  - type
  - name
  - autocomplete
  - autofocus | bolean, Um por página
  - disabled | bolean
  - readonly | bolean
  - value
  - form | linkar um input com um formulário
  - name
  - required | bolean
  - placeholder
 
 ## `<input type="password">`
 
 ### Atributos
  - minlength/maxlength | *Número mínimo e/ou máximo de caracteres para este campo*
  - size | *O númeor aceitáivel que este campo deverá conter*
  - pattern | *Expressão regular, para verificar o que está sendo digitado no campo*, *Altamente recomendando o uso de um padrão de segurança alta de senhas*,  __*exemplo: queremos que a senha contenha caracteres hexadecimais com o limite de no mínimo 4 e o máximo 8 caracteres `patern="[0-9a-fA-F]{4-8}"`*__
  - inputmode | *poderá alterar o uso do teclado em smartphones*, __*exemplo: queremos que o usuário só coloque números `inputmode="numeric"`*__

 ## `<input type="email">`
  - Espera que o usuário insira um e-mail
  - Irá validar se o valor inserido é um e-mail

 ### Atributos
  - placeholder
  - readonly
  - value
  - required
  - multiple | *O campo irá receber 1 ou mais e-mails, separado por vírgulas*
  - minlength/maxlength | *O mínino e/ou máximo valor que o campo irá conter*
  - size
  - pattern
  - list | *O id de uma `<datalist>` que está no mesmo documentos*, *`<datalist>` irá conter uma lista de valores pré-definidos a fim de sugerir ao usuário, quais valores estão disponíveis(Os valores que não forem compátiveis com o campo, não serão apresentados como sugestão)*

 ## `<input type="url">`
 - Espera que o usuário digite uma url
 - Irá validar se o valor inserido é uma url

 ### Atributos
  - placeholder
  - readonly
  - value
  - required
  - minlength/maxlength
  - size
  - pattern
  - list
  - spellcheck | *Habilitar a verificação ortográfica para este input*

 ## `<input type="file">`
  - O usuário poderá escolher 1 ou mais arquivos para enviar no formulário

 ### Atributos
  - value
  - accept | *descreve quais são os tipo aceitos*, __*exemplo: .doc, .pdf, image/png, .png*__
  - files | *A lista de arquivos ou arquivos*
  - multiple | *Permite o envio de múltiplos arquivos*
  
 **#### Envio dos arquivos**
  - Para envio dos arquivos o formulário deverá utilizaqr o método POST e o atributo encytype como `encytype="multipart/form-data"`

 ## `<input type="color">`
  - Interface para selecionar cor
  - Color Picker

 ### Atributos
  - value: RGB | Se inválido o preto será exibido
  - list

 ## `<input type="checkbox">`
  - Caixas que podem ser marcadas
  - Selecionar um valor para ser enviado
  - Se não selecionado, não será enviado nenhuem dado

 ### Atributos
  - Globais
  - value | *Valor que aquele campo contém, se não declarado, o padrão é "on"
  - checked | *Para deixar o campo marcado como padrão*

 ### Multíplos valores
  - É utilizado o atributo 'name' com o mesmo nome para os diversos campos

 ## `<input type="hidden">`
  - Invisível ao usuário
  - será enviado com o formulário
  - não receberá foco
  - leitores de tela não percebem este campo

 ## `<input type="radio">`
  - Projetado para selecionar uma única opção de um grupo de opções

 ### Atributos essenciais
  - checked | *Indica que o campo foi marcado*
  - value | *valor que este campo contém*

 ## `<input type="textarea">`
  - Mais de uma linha
  - Útil para textos grandes

 ### Atributos
  - rows/cols
  - minlength/maxlength
  - wrap
  - ... outros comuns aos inputs

 ## `<input type="select">`
  - Controle que fornece um menu de opções
  - `<option>`
    - Contém as opções a serem selecionadas
    - Atributos necessários: **value**

 ### Atributos únicos 
  - multiple | *Habilita múltiplas opções*
  - size | *Quantas opções visíveis?*

 ## `<input type="optgroup">`
  - Aplicado com o `<input type="select>`
  - Aplicado dentro de um `type="select"` para agrupar as `<option>`

 ### Atributos
  - label | *Usado para definir o título do agrupamento*

 ## `<input type="search">`
  - Para campos de buscas
  - É igual ao `type="text"`, mas poderá ser um pouco diferente dependendo do user agent

 ### Atributos
  - list
  - pattern
  - aria-label | *Empregado quando não se tem uma tag label para especificar o campo*

 ## `<input type="number">`
  - Entrada de número

 ### Atributos
  - min/max
  - step

 ## `<input type="range">`
  - Controle para selecionar um valor numérico
  - Slider ou dial control

 ### Atributos 
  - min/max
  - step
