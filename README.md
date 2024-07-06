# Refinando-um-Projeto-Conceitual-de-Banco-de-Dados-E-COMMERCE

Modificações no Banco de Dados foram:

1. Cliente PJ e PF:
Visando maior flexibilidade e organização dos dados de clientes, foi criada uma nova tabela chamada TipoCliente, contendo os seguintes campos:
idTipoCliente (chave primária) - identificador único para cada tipo de cliente.
Descricao - descrição do tipo de cliente (ex: "Pessoa Física", "Pessoa Jurídica").
Na tabela Cliente, os campos CNPJ e CPF serão removidos. Em substituição, será adicionado o campo idTipoCliente (chave estrangeira), referenciando a tabela TipoCliente. 

2. Pagamento:
Para permitir o cadastro de múltiplas formas de pagamento por cliente, são criadas duas novas tabelas:
FormaPagamento:
idFormaPagamento (chave primária) - identificador único para cada forma de pagamento.
Descricao - descrição da forma de pagamento (ex: "Cartão de Crédito", "Boleto", "Pix").
ClienteFormaPagamento:
idCliente (chave estrangeira) - referência à tabela Cliente.
idFormaPagamento (chave estrangeira) - referência à tabela FormaPagamento.
Essa tabela intermediária fará a associação de um cliente a várias formas de pagamento.

3. Entrega:
Na tabela Pedido, são adicionados os seguintes campos para registrar informações sobre a entrega:
StatusEntrega - indicará o status da entrega (ex: "Em processamento", "Enviado", "Entregue").
CodigoRastreio (opcional) - armazenará o código de rastreio da entrega, caso disponível.


Aguardo retorno.
