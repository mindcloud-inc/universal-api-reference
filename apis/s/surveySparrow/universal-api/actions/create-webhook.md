# SurveySparrow: Create Webhook

Creates a new webhook in SurveySparrow.

```
POST https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveySparrow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "surveyId": 1,
  "httpMethod": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "surveyId": 1,
    "httpMethod": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Webhook name |
| `description` | string | no | Webhook description |
| `url` | string | yes | Webhook URL |
| `eventType` | string | no | Webhook event type |
| `objectType` | string | no | Object type |
| `surveyId` | number | yes | Survey ID |
| `httpMethod` | list | yes | HTTP method |
| `headers[]` | array<object> | no | Header array |
| `type` | string | no | Webhook type |
| `payload` | object | no | Payload object |
| `includePartialSubmission` | boolean | no | Include partial submissions |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "disabled": true,
      "event_type": "string",
      "headers": [
        {}
      ],
      "http_method": "string",
      "id": 1,
      "name": "Ava Chen",
      "object_type": "string",
      "properties": {},
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `disabled` | boolean |  |
| `event_type` | string |  |
| `headers` | array<object> |  |
| `http_method` | string |  |
| `id` | number |  |
| `name` | string |  |
| `object_type` | string |  |
| `properties` | object |  |
| `url` | string |  |

## Native endpoint

Through the native SurveySparrow API, this operation is `POST /webhooks` (base URL `https://api.surveysparrow.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

