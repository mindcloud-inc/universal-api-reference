# Kite Suite: Api to send message to Project Group



```
POST https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/api-to-send-message-to-project-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/api-to-send-message-to-project-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "conversationID": "string",
  "message": "string",
  "taggedMessage": "string",
  "taggedUsers[]": [
    "string"
  ],
  "files[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/api-to-send-message-to-project-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "conversationID": "string",
    "message": "string",
    "taggedMessage": "string",
    "taggedUsers[]": ["string"],
    "files[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `conversationID` | string | yes |  |
| `message` | string | yes |  |
| `taggedMessage` | string | yes |  |
| `taggedUsers[]` | array | yes |  |
| `files[]` | array | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Kite Suite API returns.

## Native endpoint

Through the native Kite Suite API, this operation is `POST /api/v1/chat` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/api-to-send-message-to-project-group.md) for the provider-specific parameters and requirements.

