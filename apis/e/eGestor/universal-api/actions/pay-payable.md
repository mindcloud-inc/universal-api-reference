# eGestor: Pay Payable

Marks a payable as paid in eGestor.

```
PUT https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/pay-payable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/pay-payable" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "codigo": 1,
  "valor": 1,
  "dtPgto": "string",
  "dtComp": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/pay-payable', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "codigo": 1,
    "valor": 1,
    "dtPgto": "string",
    "dtComp": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `codigo` | number | yes |  |
| `valor` | number | yes |  |
| `dtPgto` | string | yes |  |
| `dtComp` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "fields": "string",
      "msg": "string",
      "obs": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | HTTP-style success code returned by eGestor. |
| `fields` | string | Field-level details when present. |
| `msg` | string | Provider message describing the payable payment result. |
| `obs` | string | Additional provider notes when present. |

## Native endpoint

Through the native eGestor API, this operation is `PUT /pagamentos/:codigo/pagar` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pay-payable.md) for the provider-specific parameters and requirements.

