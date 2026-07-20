# eGestor: List Sales

Retrieves a list of sales from eGestor.

```
GET https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/list-sales
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/list-sales?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/list-sales?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filtro` | string | no | Busca por código, palavras-chave e nome do cliente. Example: `MindCloud`. |
| `dtTipo` | list | no | Define qual data será usada nos filtros de intervalo. One of: `dtCad`, `dtEntrega`, `dtVenda`. Example: `dtVenda`. |
| `dtIni` | string | no | Data inicial no formato YYYY-MM-DD. Example: `2026-04-01`. |
| `dtFim` | string | no | Data final no formato YYYY-MM-DD. Example: `2026-04-30`. |
| `vendedor` | number | no | Código do vendedor. Example: `1`. |
| `tipo` | list | no | Filtra por orçamento ou venda. One of: `10`, `50`. Example: `50`. |
| `formaPgto` | number | no | Filtra pela forma de pagamento dos financeiros da venda. Example: `2`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contaDest` | number | no | Filtra pela conta destino dos financeiros da venda. Example: `1`. |
| `situOS` | string | no | Filtra pela situação da venda ou ordem de serviço. Example: `Em espera`. |
| `buscaObs` | string | no | Pesquisa nas observações da venda. Example: `instalação`. |
| `fiscal` | list | no | Filtra vendas com ou sem nota fiscal. One of: `comNFe`, `semNFe`. Example: `semNFe`. |
| `listarCanceladas` | number | no | Inclui vendas canceladas na listagem. Example: `1`. |
| `fields` | string | no | Campos retornados pela listagem, separados por vírgula. Example: `codigo,nomeContato,valorTotal`. |
| `orderBy` | string | no | Campo e direção de ordenação, separados por vírgula. Example: `dtVenda,asc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentPage": 1,
      "data": [
        {
          "ativo": true,
          "codContato": 1,
          "codigo": 1,
          "codVendedor": 1,
          "dtVenda": "2026-05-07T12:00:00.000Z",
          "nomeContato": "string",
          "situacao": 1,
          "valorFinanc": 1,
          "valorTotal": 1
        }
      ],
      "from": 1,
      "lastPage": 1,
      "nextPageUrl": {},
      "perPage": 1,
      "prevPageUrl": {},
      "to": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPage` | number |  |
| `data[].ativo` | boolean |  |
| `data[].codContato` | number |  |
| `data[].codigo` | number |  |
| `data[].codVendedor` | number |  |
| `data[].dtVenda` | date |  |
| `data[].nomeContato` | string |  |
| `data[].situacao` | number |  |
| `data[].valorFinanc` | number |  |
| `data[].valorTotal` | number |  |
| `from` | number |  |
| `lastPage` | number |  |
| `nextPageUrl` | object |  |
| `perPage` | number |  |
| `prevPageUrl` | object |  |
| `to` | number |  |
| `total` | number |  |

## Native endpoint

Through the native eGestor API, this operation is `GET /vendas` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sales.md) for the provider-specific parameters and requirements.

