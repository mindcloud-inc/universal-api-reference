# eGestor: Create Receivable

Creates a new receivable in eGestor.

```
POST https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/create-receivable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/create-receivable" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "codPlanoContas": 1,
  "descricao": "string",
  "valor": 1,
  "dtVenc": "string",
  "dtComp": "string",
  "codDisponivel": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/create-receivable', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `codPlanoContas` | number | yes | Internal account plan code linked to the receivable. |
| `numDoc` | string | no | Document number for the receivable. |
| `descricao` | string | yes | Receivable description. |
| `valor` | number | yes | Receivable amount. |
| `dtVenc` | string | yes | Receivable due date in yyyy-mm-dd format. |
| `dtComp` | string | yes | Competence date in yyyy-mm-dd format. |
| `recebido` | boolean | no | Whether the receivable is already received. Default: `false`. |
| `codDisponivel` | number | yes | Internal cash account code. |
| `obs` | string | no | Additional receivable notes. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `codFormaPgto` | number | no | Internal payment method code for the receivable. |
| `dtPgto` | string | no | Payment date in yyyy-mm-dd format. |
| `dtCred` | string | no | Credit date in yyyy-mm-dd format. |
| `codContato` | number | no | Internal contact code. |
| `tags` | list<string> | no | Tags to attach to the receivable. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "codigo": 1,
      "codModulo": 1,
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
| `codigo` | number |  |
| `codModulo` | number |  |
| `origem` | string |  |
| `situacao` | number |  |

## Native endpoint

Through the native eGestor API, this operation is `POST /recebimentos` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-receivable.md) for the provider-specific parameters and requirements.

