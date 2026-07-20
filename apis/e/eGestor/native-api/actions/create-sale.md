# Create Sale with eGestor

Creates a new sale in eGestor.

## Endpoint

- **Method:** `POST`
- **Path:** `/vendas`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [Create Sale](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L3630)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `codContato` | body | `number` | yes | Código do contato cliente da venda. |
| `codVendedor` | body | `number` | yes | Código do vendedor da venda. |
| `dtVenda` | body | `string` | yes | Data da venda no formato YYYY-MM-DD. |
| `dtEntrega` | body | `string` | no | Data de entrega no formato YYYY-MM-DD. |
| `situacao` | body | `list` | yes | Situação da venda, como orçamento ou venda efetivada. Accepted values: `10`, `50`. |
| `tags[]` | body | `array<string>` | no | Tags da venda. |
| `valorFrete` | body | `number` | no | Valor do frete da venda. |
| `valorDesc` | body | `number` | no | Valor do desconto da venda. |
| `valorDespesasAcessorias` | body | `number` | no | Valor das despesas acessórias da venda. |
| `clienteFinal` | body | `boolean` | no | Define se o contato é cliente final. |
| `enderecoEntrega` | body | `number` | no | Código do endereço de entrega associado ao contato. |
| `situacaoOS` | body | `string` | no | Situação da ordem de serviço quando aplicável. |
| `customizado` | body | `object` | no | Objeto com campos personalizados da venda. |
| `produtos[]` | body | `array<object>` | yes | Lista de produtos da venda. |
| `financeiros[]` | body | `array<object>` | no | Lista de recebimentos financeiros da venda. |
| `despesas[]` | body | `array<object>` | no | Lista de despesas associadas à venda. |
