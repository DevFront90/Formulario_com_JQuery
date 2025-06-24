# 📝 Formulário com jQuery

Projeto simples e funcional que demonstra como manipular formulários com jQuery. Ao submeter os dados preenchidos, eles são capturados e exibidos dinamicamente no corpo da página, sem recarregamento.

---

## 🚀 Demonstração

Preencha os campos do formulário e clique em **Enviar**. Os dados serão exibidos diretamente na área de conteúdo da página.

---

## 💡 Funcionalidades

- Captura de dados de formulário com jQuery
- Exibição dinâmica das informações no DOM
- Submissão sem recarregamento da página
- Uso de boas práticas com jQuery para manipulação do DOM

---

## 🛠️ Tecnologias Utilizadas

- HTML5
- CSS3
- [jQuery](https://jquery.com/)

---

## 📦 Estrutura do Projeto

Formulario_com_JQuery/
├── css/
│ └── style.css # Estilização do formulário
├── js/
│ └── script.js # Script com jQuery para captura e exibição dos dados
├── index.html # Estrutura principal do formulário

kotlin
Copiar
Editar

---

## 🧠 Lógica de Funcionamento

O script em jQuery intercepta o envio do formulário e realiza as seguintes ações:

```javascript
$(function() {
  $('.form_contato').submit(function() {

    var container = $('.container');

    var content = 'Nome: ' + $('input[name=nome]').val() +
                  '<hr>Email: ' + $('input[name=email]').val() +
                  '<hr>Telefone: ' + $('input[name=telefone]').val();

    container.html(content);

    return false; // Impede o envio padrão do formulário
  });
});
📌 Explicação técnica:
$(function() {...}): Aguarda o carregamento completo do DOM.

.submit(function() {...}): Escuta o envio do formulário.

$('input[name=...]').val(): Captura os valores digitados nos campos de entrada.

container.html(content): Insere os dados formatados no container da página.

return false: Bloqueia o comportamento padrão de recarregar a página.

📷 Exemplo de Saída
text
Copiar
Editar
Nome: João da Silva
----------------------------
Email: joao@email.com
----------------------------
Telefone: (24) 99999-9999
