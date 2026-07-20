# Printify: Simulate Webhook

Simulates a webhook in Printify.

```
PUT https://connect.mindcloud.co/v1/universal/printify/latest/actions/simulate-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/printify/latest/actions/simulate-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shop_id": "27141936",
  "webhook_id": "69d9636798c77b61480a2daa"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printify/latest/actions/simulate-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shop_id": "27141936",
    "webhook_id": "69d9636798c77b61480a2daa"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `anything` | string | no | Arbitrary payload echoed in the simulated webhook resource. Default: `test`. |
| `shop_id` | number | yes | Printify shop id. Default: `27141936`. |
| `webhook_id` | string | yes | Printify webhook id. Default: `69d9636798c77b61480a2daa`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Printify API, this operation is `POST /shops/:shop_id/webhooks/:webhook_id/simulate` (base URL `https://api.printify.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/simulate-webhook.md) for the provider-specific parameters and requirements.

