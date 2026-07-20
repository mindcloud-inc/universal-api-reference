# CloudConvert: Create Webhook

Creates a webhook in your CloudConvert account.

```
POST https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudConvert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "events[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "events[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Webhook URL to send notifications to. |
| `events[]` | array<string> | yes | One or more webhook events to subscribe to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "disabled": true,
      "events": [
        "string"
      ],
      "failing": true,
      "id": 1,
      "lastErrorAt": "string",
      "lastResponseCode": "string",
      "links": {
        "self": "https://example.com"
      },
      "signingSecret": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `disabled` | boolean |  |
| `events` | array<string> |  |
| `failing` | boolean |  |
| `id` | number |  |
| `lastErrorAt` | string |  |
| `lastResponseCode` | string |  |
| `links.self` | string |  |
| `signingSecret` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native CloudConvert API, this operation is `POST /webhooks` (base URL `https://api.cloudconvert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

