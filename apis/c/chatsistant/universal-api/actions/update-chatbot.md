# Chatsistant: Update Chatbot

Updates an existing chatbot in Chatsistant.

```
PUT https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/update-chatbot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatsistant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/update-chatbot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/update-chatbot', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | no | The model name. |
| `name` | string | no | The chatbot name. |
| `prompt` | string | no | The chatbot prompt. |
| `temperature` | string | no | The chatbot temperature. |
| `uuid` | string | no | The chatbot UUID. |
| `visibility` | string | no | The chatbot visibility. |

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

Through the native Chatsistant API, this operation is `POST /chatbot/:uuid/update` (base URL `https://app.chatsistant.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-chatbot.md) for the provider-specific parameters and requirements.

