# Everbill: Add Bill Transaction

Creates a new bill transaction in Everbill.

```
POST https://connect.mindcloud.co/v1/universal/everbill/latest/actions/add-bill-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Everbill `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/everbill/latest/actions/add-bill-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/everbill/latest/actions/add-bill-transaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Everbill record ID. |
| `sum` | number | no | sum request body field. |
| `date` | string | no | date request body field. |
| `type` | string | yes | type request body field. |
| `notes` | string | no | notes request body field. |
| `show` | boolean | no | show request body field. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Everbill API returns.

## Native endpoint

Through the native Everbill API, this operation is `POST /bills/add_transaction/:id` (base URL `https://api.everbill.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-bill-transaction.md) for the provider-specific parameters and requirements.

