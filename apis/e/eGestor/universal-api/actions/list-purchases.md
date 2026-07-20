# eGestor: List Purchases

Retrieves a list of purchases from eGestor.

```
GET https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/list-purchases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/list-purchases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/list-purchases?${params}`, {
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
| `filtro` | string | no | Busca a string informada nos campos código da compra, palavras-chave e nome do fornecedor. Example: `MindCloud Purchase Supplier 20260401`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentPage": 1,
      "data": [
        {
          "ativo": 1,
          "codContato": 1,
          "codigo": 1,
          "dtCompra": "2026-05-07T12:00:00.000Z",
          "dtEntrega": "2026-05-07T12:00:00.000Z",
          "nomeContato": "string",
          "numNota": "string",
          "obs": "string",
          "situacao": 1,
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
| `data[].ativo` | number |  |
| `data[].codContato` | number |  |
| `data[].codigo` | number |  |
| `data[].dtCompra` | date |  |
| `data[].dtEntrega` | date |  |
| `data[].nomeContato` | string |  |
| `data[].numNota` | string |  |
| `data[].obs` | string |  |
| `data[].situacao` | number |  |
| `data[].valorTotal` | number |  |
| `from` | number |  |
| `lastPage` | number |  |
| `nextPageUrl` | object |  |
| `perPage` | number |  |
| `prevPageUrl` | object |  |
| `to` | number |  |
| `total` | number |  |

## Native endpoint

Through the native eGestor API, this operation is `GET /compras` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-purchases.md) for the provider-specific parameters and requirements.

