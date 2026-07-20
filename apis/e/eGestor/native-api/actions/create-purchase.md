# Create Purchase with eGestor

Creates a new purchase in eGestor.

## Endpoint

- **Method:** `POST`
- **Path:** `/compras`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [Create Purchase](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L3179)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `codContato` | body | `number` | yes | Código do fornecedor da compra. |
| `numNota` | body | `string` | no | Número do documento fiscal. |
| `dtCompra` | body | `string` | yes | Data da realização da compra no formato YYYY-MM-DD. |
| `dtEntrega` | body | `string` | no | Data da entrega no formato YYYY-MM-DD. |
| `situacao` | body | `number` | yes | Situação da compra. Use 10 para orçamento ou 50 para compra efetivada. Accepted values: `10`, `50`. |
| `atualizarPrecoVenda` | body | `boolean` | yes | Define se o preço de venda será atualizado. |
| `produtos[]` | body | `array<object>` | yes | Lista de itens da compra. Cada item deve incluir codProduto, custoBruto, quant, vDesc, valorIPI e valorST. |
| `financeiros[]` | body | `array<object>` | no | Lista de lançamentos financeiros quando aplicável. |
