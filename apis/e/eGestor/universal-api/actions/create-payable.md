# eGestor: Create Payable

Creates a new payable in eGestor.

```
POST https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/create-payable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/create-payable" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/create-payable', {
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
| `codPlanoContas` | number | yes |  |
| `numDoc` | string | no |  |
| `descricao` | string | yes |  |
| `valor` | number | yes |  |
| `dtVenc` | string | yes |  |
| `dtComp` | string | yes |  |
| `pago` | boolean | no | Default: `false`. |
| `codDisponivel` | number | yes |  |
| `obs` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `codFormaPgto` | number | no |  |
| `dtPgto` | string | no |  |
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
| `codigo` | number | Internal payable code. |
| `codModulo` | number | Source module record code. |
| `descricao` | string | Created payable description. |
| `origem` | string | Source module for the payable. |
| `situacao` | number | Payable status after creation. |

## Native endpoint

Through the native eGestor API, this operation is `POST /pagamentos` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payable.md) for the provider-specific parameters and requirements.

