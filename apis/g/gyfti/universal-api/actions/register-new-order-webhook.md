# gyfti: Register New Order Webhook

Registers a new order webhook in gyfti.

```
POST https://connect.mindcloud.co/v1/universal/gyfti/latest/actions/register-new-order-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a gyfti `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gyfti/latest/actions/register-new-order-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hookUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gyfti/latest/actions/register-new-order-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hookUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hookUrl` | string | yes | Destination URL that gyfti should call when a new order is created. |
| `user` | string | no | Optional gyfti user email associated with the webhook registration. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Campaign Name": "Ava Chen",
      "Charity": "string",
      "Cost excl tax": 1,
      "Cost incl tax": 1,
      "Created date": "2026-05-07T12:00:00.000Z",
      "Order Status": "string",
      "Product Name": "Ava Chen",
      "Recipient Email": "ava@example.com",
      "Recipient First Name": "Ava",
      "Recipient Last Name": "Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Campaign Name` | string |  |
| `Charity` | string |  |
| `Cost excl tax` | number |  |
| `Cost incl tax` | number |  |
| `Created date` | date |  |
| `Order Status` | string |  |
| `Product Name` | string |  |
| `Recipient Email` | string |  |
| `Recipient First Name` | string |  |
| `Recipient Last Name` | string |  |

## Native endpoint

Through the native gyfti API, this operation is `POST /wf/new_hook_order/` (base URL `https://app.gyfti.fr/api/1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/register-new-order-webhook.md) for the provider-specific parameters and requirements.

