# Channex: Update Webhook

Updates an existing webhook in Channex.

```
PUT https://connect.mindcloud.co/v1/universal/channex/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/channex/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "webhook": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/channex/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "webhook": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | UUID of the webhook to update. |
| `webhook` | object | yes | Top-level webhook payload object documented by Channex for webhook updates. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "attributes": {
          "callback_url": "https://example.com",
          "event_mask": "string",
          "is_active": true,
          "send_data": true
        },
        "id": "string",
        "relationships": {
          "property": {
            "data": {
              "id": "string"
            }
          }
        },
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.attributes.callback_url` | string |  |
| `data.attributes.event_mask` | string |  |
| `data.attributes.is_active` | boolean |  |
| `data.attributes.send_data` | boolean |  |
| `data.id` | string |  |
| `data.relationships.property.data.id` | string |  |
| `data.type` | string |  |

## Native endpoint

Through the native Channex API, this operation is `PUT /webhooks/:id` (base URL `https://staging.channex.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

