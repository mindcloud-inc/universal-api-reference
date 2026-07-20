# Uspacy: Create Outgoing Webhook

Creates a new outgoing webhook in Uspacy.

```
POST https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/create-outgoing-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uspacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/create-outgoing-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "events[].service": "string",
  "events[].type": "string",
  "events[].actions[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/create-outgoing-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "events[].service": "string",
    "events[].type": "string",
    "events[].actions[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | The outgoing webhook target URL. |
| `events[].service` | string | yes | Webhook event service. |
| `events[].type` | string | yes | Webhook event type. |
| `events[].actions[]` | array<string> | yes | Webhook event actions. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `events[].table_name` | string | no | Optional CRM table name for entity CRM events. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": 1,
      "id": 1,
      "updated_at": 1,
      "url": "https://example.com",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | number |  |
| `id` | number |  |
| `updated_at` | number |  |
| `url` | string |  |
| `user_id` | number |  |

## Native endpoint

Through the native Uspacy API, this operation is `POST /company/v1/webhooks` (base URL `https://{{credentials.site}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-outgoing-webhook.md) for the provider-specific parameters and requirements.

