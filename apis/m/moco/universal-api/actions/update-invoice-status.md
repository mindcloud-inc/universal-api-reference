# Moco: Update Invoice Status



```
PUT https://connect.mindcloud.co/v1/universal/moco/latest/actions/update-invoice-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moco/latest/actions/update-invoice-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moco/latest/actions/update-invoice-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |
| `status` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Moco API returns.

## Native endpoint

Through the native Moco API, this operation is `PUT /invoices/:id/update_status` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice-status.md) for the provider-specific parameters and requirements.

