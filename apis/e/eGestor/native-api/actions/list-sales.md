# List Sales with eGestor

Retrieves a list of sales from eGestor.

## Endpoint

- **Method:** `GET`
- **Path:** `/vendas`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [List Sales](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L3551)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filtro` | query | `string` | no | Busca por código, palavras-chave e nome do cliente. |
| `dtTipo` | query | `list` | no | Define qual data será usada nos filtros de intervalo. Accepted values: `dtCad`, `dtEntrega`, `dtVenda`. |
| `dtIni` | query | `string` | no | Data inicial no formato YYYY-MM-DD. |
| `dtFim` | query | `string` | no | Data final no formato YYYY-MM-DD. |
| `vendedor` | query | `number` | no | Código do vendedor. |
| `tipo` | query | `list` | no | Filtra por orçamento ou venda. Accepted values: `10`, `50`. |
| `formaPgto` | query | `number` | no | Filtra pela forma de pagamento dos financeiros da venda. |
| `contaDest` | query | `number` | no | Filtra pela conta destino dos financeiros da venda. |
| `situOS` | query | `string` | no | Filtra pela situação da venda ou ordem de serviço. |
| `buscaObs` | query | `string` | no | Pesquisa nas observações da venda. |
| `fiscal` | query | `list` | no | Filtra vendas com ou sem nota fiscal. Accepted values: `comNFe`, `semNFe`. |
| `listarCanceladas` | query | `number` | no | Inclui vendas canceladas na listagem. |
| `fields` | query | `string` | no | Campos retornados pela listagem, separados por vírgula. |
| `orderBy` | query | `string` | no | Campo e direção de ordenação, separados por vírgula. |
