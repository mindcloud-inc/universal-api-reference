# DONNAJAMES Easy: Update Chatbot

Updates an existing chatbot in DONNAJAMES Easy.

```
PUT https://connect.mindcloud.co/v1/universal/dONNAJAMESEasy/latest/actions/update-chatbot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DONNAJAMES Easy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dONNAJAMESEasy/latest/actions/update-chatbot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dONNAJAMESEasy/latest/actions/update-chatbot', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no |  |
| `rateLimitMessage` | string | no |  |
| `uuid` | string | yes | Chatbot uuid |
| `visibility` | string | no |  |
| `showCitations` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "meta": {},
      "modified_at": "string",
      "name": "Ava Chen",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `meta` | object |  |
| `modified_at` | string |  |
| `name` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native DONNAJAMES Easy API, this operation is `POST chatbot/:uuid/update` (base URL `https://app.gpt-trainer.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-chatbot.md) for the provider-specific parameters and requirements.

