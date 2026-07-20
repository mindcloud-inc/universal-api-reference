# Evalandgo: Create Webhook

Creates a new webhook in Evalandgo.

```
POST https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evalandgo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "questionnaire": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "questionnaire": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `questionnaire` | string | yes |  |
| `name` | string | no |  |
| `url` | string | no |  |
| `events[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@context": "string",
      "@id": "string",
      "@type": "string",
      "active": true,
      "createAt": "string",
      "events": [
        "string"
      ],
      "id": 1,
      "name": "Ava Chen",
      "questionnaire": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@context` | string |  |
| `@id` | string |  |
| `@type` | string |  |
| `active` | boolean |  |
| `createAt` | string |  |
| `events[]` | string |  |
| `id` | number |  |
| `name` | string |  |
| `questionnaire` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Evalandgo API, this operation is `POST /api/v3/webhooks` (base URL `https://app.evalandgo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

