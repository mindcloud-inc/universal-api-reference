# Channex: Get Webhook

Retrieves an existing webhook from Channex.

```
GET https://connect.mindcloud.co/v1/universal/channex/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/channex/latest/actions/get-webhook?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/channex/latest/actions/get-webhook?${params}`, {
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
| `id` | string | yes | UUID of the webhook to retrieve. |

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

Through the native Channex API, this operation is `GET /webhooks/:id` (base URL `https://staging.channex.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

