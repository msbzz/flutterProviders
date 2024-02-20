# Gerenciando estados com Provider

Este projeto é fruto do curso de 'Flutter : gerenciamento de estados com Provider' da plataforma ALURA

## Introdução

Dado o aplicativo 'clients_control' onde é carregado diretamente por listas dentro dos widgets 'ClientsPage' e 'ClientTypesPage' a ideia e apresentar o uso de "Provider"
como meio de integração da informação na arvore de widgets.



Abaixo segue a interface da aplicação

<table style="width: 100%; border-collapse: collapse;" border="0">
  <tr>
    <td style="border: none; width: 10%;"> <img src="info/cadasro_cliente_01.png" alt="cadastro" style="width: 100%; display: block;"/></td>
    <td style="border: none; width: 10%;"> <img src="info/cadasro_cliente_02.png" alt="primeiro teste sucesso" style="width: 100%; display: block;"/></td>
    <td style="border: none; width: 10%;"> <img src="info/drawer_menu.png" alt="hamburger menu" style="width: 100%; display: block;"/></td>
    <td style="border: none; width: 10%;"> <img src="info/tipo_cliente_01.png" alt="tipo cliente" style="width: 100%; display: block;"/></td>
    <td style="border: none; width: 10%;"> <img src="info/tipo_cliente_02.png" alt="novo tipo cliente" style="width: 100%; display: block;"/></td>
    <td style="border: none; width: 10%;"> <img src="info/tipo_cliente_03.png" alt="icone tipo cliente" style="width: 100%; display: block;"/></td>
    <td style="border: none; width: 10%;"> <img src="info/tipo_cliente_04.png" alt="tipo cliente 4" style="width: 100%; display: block;"/></td>
  </tr>
</table>

- Listas fixas nos widgets


   - ClientsPage

 
    <img src="info/array_clientes.png" alt="pagina de clientes" style="width: 100%; display: block;"/>

     
   - ClientTypesPage
 
     <img src="info/array_tipo_clientes.png" alt="pagina tipo de clientes" style="width: 100%; display: block;"/>


 ## Integração com a single source of true (ssot)

   Adaptação "main()" onde é passado um item de array simulando uma futura carga, na pagina de "ClientsPage()" é feita a remoção do array "clients" assim como adaptada a utilização do provider na apresentação e no botão de adição do "alert dialog". 

   - Alteração na "Main()"

   <img src="info/main.provider.png" alt="" style="width: 100%; display: block;"/>

   - Alteração em "ClientsPage()"

     listview.builder

   <img src="info/listView.builder.provider.png" alt="" style="width: 100%; display: block;"/>

    alertDialog

   <img src="info/alert dialog,actions.textbutton.onpress.consumer.png" alt="" style="width: 100%; display: block;"/>


 ##  Aplicando boas práticas  

   Se trata ótima prática atribuir a responsabilidade de adicionar, modificar, excluir os dados de uma model para a model, não pelo aplicativo do pois foi só uma forma didática, em vez de chamar o add do lista criar um método para isso na propria classe Clients.

   
   ClientsPage / add

   <img src="info/clients_page.modiffy.add.png" alt="" style="width: 100%; display: block;"/>


   Clients / add

   <img src="info/clients.changeNotifier.add.png" alt="" style="width: 100%; display: block;"/>




