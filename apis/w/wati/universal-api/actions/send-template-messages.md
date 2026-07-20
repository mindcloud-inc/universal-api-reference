# Wati: Send Template Messages

Sends template messages to multiple contacts in Wati.

```
POST https://connect.mindcloud.co/v1/universal/wati/latest/actions/send-template-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wati `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wati/latest/actions/send-template-messages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateName": "Ava Chen",
  "broadcastName": "Ava Chen",
  "receivers[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wati/latest/actions/send-template-messages', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateName": "Ava Chen",
    "broadcastName": "Ava Chen",
    "receivers[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateName` | string | yes | Approved Wati template name. |
| `broadcastName` | string | yes | Name for the broadcast record. |
| `receivers[]` | array<object> | yes | Recipients and custom parameters for the broadcast. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": {
        "error": "string",
        "invalidCustomParameters": [
          {}
        ],
        "invalidWhatsappNumbers": [
          "string"
        ]
      },
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | object | Batch validation errors returned by Wati. |
| `errors.error` | string | Top-level provider error string. |
| `errors.invalidCustomParameters` | array<object> | Custom parameter validation errors when present. |
| `errors.invalidWhatsappNumbers` | array<string> | Recipient phone numbers rejected by Wati. |
| `result` | boolean | Whether Wati accepted the batch template send. |

## Native endpoint

Through the native Wati API, this operation is `POST /api/v1/sendTemplateMessages` (base URL `{{credentials.apiEndpointUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-template-messages.md) for the provider-specific parameters and requirements.

