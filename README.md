🔍 Como funciona o código:
javascript
Copiar
Editar
$(function() {
  $('.form_contato').submit(function() {
    
    var container = $('.container'); // Seleciona o local onde os dados serão exibidos

    // Captura os valores dos inputs usando o atributo "name"
    var content = 'Nome:' + $('input[name=nome]').val() + 
                  '<hr>Email:' + $('input[name=email]').val() + 
                  '<hr>Telefone:' + $('input[name=telefone]').val();

    // Insere os dados capturados dentro do container
    container.html(content);

    return false; // Impede o envio tradicional do formulário (recarregar a página)
  });
});
🧠 O que está acontecendo:
$(function() {...}): Executa o código assim que o DOM estiver pronto.

.submit(function() {...}): Captura o evento de envio do formulário.

$('input[name=campo]').val(): Acessa o valor preenchido pelo usuário em cada campo de input.

container.html(content): Insere todo o conteúdo formatado (com <hr> separando) dentro do .container.

return false: Cancela o envio padrão do formulário para evitar que a página seja recarregada.

🧪 Exemplo visual (simulação de resultado):
Se o usuário preencher:

Nome: João

Email: joao@email.com

Telefone: (24) 99999-9999

O container receberá:

markdown
Copiar
Editar
Nome: João
-----------------------
Email: joao@email.com
-----------------------
Telefone: (24) 99999-9999
