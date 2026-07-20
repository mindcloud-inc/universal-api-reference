# Filestage: Add New Webhook

Creates a new webhook in Filestage.

```
POST https://connect.mindcloud.co/v1/universal/filestage/latest/actions/add-new-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Filestage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/filestage/latest/actions/add-new-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookUrl": "https://example.com",
  "events[]": [
    "string"
  ],
  "headers": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filestage/latest/actions/add-new-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhookUrl": "https://example.com",
    "events[]": ["string"],
    "headers": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookUrl` | string | yes |  |
| `events[]` | array<string> | yes |  |
| `headers` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        "string"
      ],
      "headers": {},
      "id": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events` | array<string> |  |
| `headers` | object |  |
| `id` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Filestage API, this operation is `POST /webhooks` (base URL `https://api.filestage.io/ext/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-new-webhook.md) for the provider-specific parameters and requirements.

