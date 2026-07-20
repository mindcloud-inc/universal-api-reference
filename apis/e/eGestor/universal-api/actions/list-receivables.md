# eGestor: List Receivables

Retrieves a list of receivables from eGestor.

```
GET https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/list-receivables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/list-receivables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/list-receivables?${params}`, {
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
| `filtro` | string | no | Searches by receivable code, description, tags, or customer name. |
| `dtIni` | string | no | Start date in yyyy-mm-dd format. |
| `dtFim` | string | no | End date in yyyy-mm-dd format. |
| `orderBy` | string | no | Single sort definition in campo,direcao format. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dtTipo` | string | no | Date field used by dtIni and dtFim. |
| `caixa` | number | no | Internal cash account code. |
| `origem` | string | no | Receivable origin. |
| `conciliacao` | string | no | Bank reconciliation filter. |
| `planoContas` | number | no | Linked account plan code. |
| `obs` | string | no | Searches additional receivable notes. |
| `formaPgto` | number | no | Internal payment method code. |
| `numDoc` | string | no | Document number filter. |
| `situFin` | number | no | Receivable financial status code. |
| `boleto` | string | no | Filters receivables with or without boleto. |
| `recibo` | string | no | Filters receivables with or without receipt. |
| `fields` | string | no | Comma-separated response fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentPage": 1,
      "data": [
        {
          "codigo": 1,
          "data": "string",
          "descricao": "string",
          "nomeContato": "string",
          "situacao": 1,
          "valor": 1
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
| `data[].codigo` | number |  |
| `data[].data` | string |  |
| `data[].descricao` | string |  |
| `data[].nomeContato` | string |  |
| `data[].situacao` | number |  |
| `data[].valor` | number |  |
| `from` | number |  |
| `lastPage` | number |  |
| `nextPageUrl` | object |  |
| `perPage` | number |  |
| `prevPageUrl` | object |  |
| `to` | number |  |
| `total` | number |  |

## Native endpoint

Through the native eGestor API, this operation is `GET /recebimentos` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-receivables.md) for the provider-specific parameters and requirements.

