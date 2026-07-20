# eGestor: Get Payable

Retrieves details for a payable from eGestor.

```
GET https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/get-payable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/get-payable?connectionId=$CONNECTION_ID&codigo=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "codigo": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/get-payable?${params}`, {
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
| `codigo` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "codContato": 1,
      "codDisponivel": 1,
      "codFormaPgto": 1,
      "codigo": 1,
      "codModulo": 1,
      "codPlanoContas": 1,
      "descricao": "string",
      "dtCad": "2026-05-07T12:00:00.000Z",
      "dtComp": "2026-05-07T12:00:00.000Z",
      "dtCred": "2026-05-07T12:00:00.000Z",
      "dtPgto": "2026-05-07T12:00:00.000Z",
      "dtVenc": "2026-05-07T12:00:00.000Z",
      "numDoc": "string",
      "obs": "string",
      "origem": "string",
      "situacao": 1,
      "taxa": 1,
      "valor": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `codContato` | number |  |
| `codDisponivel` | number |  |
| `codFormaPgto` | number |  |
| `codigo` | number |  |
| `codModulo` | number |  |
| `codPlanoContas` | number |  |
| `descricao` | string |  |
| `dtCad` | date |  |
| `dtComp` | date |  |
| `dtCred` | date |  |
| `dtPgto` | date |  |
| `dtVenc` | date |  |
| `numDoc` | string |  |
| `obs` | string |  |
| `origem` | string |  |
| `situacao` | number |  |
| `taxa` | number |  |
| `valor` | number |  |

## Native endpoint

Through the native eGestor API, this operation is `GET /pagamentos/:codigo` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payable.md) for the provider-specific parameters and requirements.

