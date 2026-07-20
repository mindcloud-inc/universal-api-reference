# eGestor: Update Receivable

Updates an existing receivable in eGestor.

```
PUT https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/update-receivable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/update-receivable" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "codigo": 1,
  "codPlanoContas": 1,
  "descricao": "string",
  "valor": 1,
  "dtVenc": "string",
  "dtComp": "string",
  "codDisponivel": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/update-receivable', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "codigo": 1,
    "codPlanoContas": 1,
    "descricao": "string",
    "valor": 1,
    "dtVenc": "string",
    "dtComp": "string",
    "codDisponivel": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `codigo` | number | yes |  |
| `codPlanoContas` | number | yes |  |
| `numDoc` | string | no |  |
| `descricao` | string | yes |  |
| `valor` | number | yes |  |
| `dtVenc` | string | yes |  |
| `dtComp` | string | yes |  |
| `codDisponivel` | number | yes |  |
| `obs` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `codFormaPgto` | number | no |  |
| `dtCred` | string | no |  |
| `codContato` | number | no |  |
| `tags` | list<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "codigo": 1,
      "codModulo": 1,
      "descricao": "string",
      "origem": "string",
      "situacao": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `codigo` | number | Internal receivable code. |
| `codModulo` | number | Source module record code. |
| `descricao` | string | Updated receivable description. |
| `origem` | string | Source module for the receivable. |
| `situacao` | number | Receivable status after the update. |

## Native endpoint

Through the native eGestor API, this operation is `PUT /recebimentos/:codigo` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-receivable.md) for the provider-specific parameters and requirements.

