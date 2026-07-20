# WEBLUCY: Create Webhook

Creates a new webhook in WEBLUCY.

```
POST https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WEBLUCY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "events[]": [
    "string"
  ],
  "secret": "string",
  "target": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "events[]": ["string"],
    "secret": "string",
    "target": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `events[]` | array<string> | yes | The webhook events to subscribe to. |
| `secret` | string | yes | The webhook secret used to sign events. |
| `target` | string | yes | The webhook destination URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        "string"
      ],
      "id": "string",
      "secret": "string",
      "target": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events` | array<string> |  |
| `id` | string |  |
| `secret` | string |  |
| `target` | string |  |

## Native endpoint

Through the native WEBLUCY API, this operation is `POST /webhooks` (base URL `https://apps.weblucy.com/api/site`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

