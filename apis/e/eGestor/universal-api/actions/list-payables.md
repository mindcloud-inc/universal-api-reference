# eGestor: List Payables

Retrieves a list of payables from eGestor.

```
GET https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/list-payables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/list-payables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/list-payables?${params}`, {
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
| `filtro` | string | no |  |
| `dtIni` | string | no |  |
| `dtFim` | string | no |  |
| `orderBy` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dtTipo` | string | no |  |
| `caixa` | number | no |  |
| `origem` | string | no |  |
| `conciliacao` | string | no |  |
| `planoContas` | number | no |  |
| `obs` | string | no |  |
| `formaPgto` | number | no |  |
| `numDoc` | string | no |  |
| `situFin` | number | no |  |
| `boleto` | string | no |  |
| `recibo` | string | no |  |
| `fields` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentPage": 1,
      "from": {},
      "lastPage": 1,
      "nextPageUrl": {},
      "perPage": 1,
      "prevPageUrl": {},
      "to": {},
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
| `from` | object |  |
| `lastPage` | number |  |
| `nextPageUrl` | object |  |
| `perPage` | number |  |
| `prevPageUrl` | object |  |
| `to` | object |  |
| `total` | number |  |

## Native endpoint

Through the native eGestor API, this operation is `GET /pagamentos` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payables.md) for the provider-specific parameters and requirements.

