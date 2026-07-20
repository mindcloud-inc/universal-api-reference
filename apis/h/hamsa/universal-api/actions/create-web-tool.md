# Hamsa: Create Web Tool

Creates a new web tool in Hamsa.

```
POST https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/create-web-tool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hamsa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/create-web-tool" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "async": true,
  "description": "string",
  "messages[]": [
    {}
  ],
  "messages[].content": "string",
  "messages[].type": "string",
  "name": "Ava Chen",
  "params": {},
  "toolSettings": {},
  "toolSettings.methodType": "string",
  "toolSettings.serverUrl": "https://example.com",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/create-web-tool', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "async": true,
    "async": true,
    "description": "string",
    "description": "string",
    "messages[]": [{}],
    "messages[]": [{}],
    "messages[].content": "string",
    "messages[].content": "string",
    "messages[].type": "string",
    "messages[].type": "string",
    "name": "Ava Chen",
    "params": {},
    "params": {},
    "toolSettings": {},
    "toolSettings": {},
    "toolSettings.methodType": "string",
    "toolSettings.methodType": "string",
    "toolSettings.serverUrl": "https://example.com",
    "toolSettings.serverUrl": "https://example.com",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `async` | boolean | yes |  |
| `async` | boolean | yes |  |
| `collectionId` | string | no |  |
| `collectionId` | string | no |  |
| `description` | string | yes |  |
| `description` | string | yes |  |
| `messages[]` | array<object> | yes |  |
| `messages[]` | array<object> | yes |  |
| `messages[].content` | string | yes |  |
| `messages[].content` | string | yes |  |
| `messages[].type` | string | yes |  |
| `messages[].type` | string | yes |  |
| `name` | string | yes |  |
| `params` | object | yes |  |
| `params` | object | yes |  |
| `toolSettings` | object | yes |  |
| `toolSettings` | object | yes |  |
| `toolSettings.authToken` | string | no |  |
| `toolSettings.authToken` | string | no |  |
| `toolSettings.httpHeaders` | object | no |  |
| `toolSettings.httpHeaders` | object | no |  |
| `toolSettings.methodType` | string | yes |  |
| `toolSettings.methodType` | string | yes |  |
| `toolSettings.pathParameters` | object | no |  |
| `toolSettings.pathParameters` | object | no |  |
| `toolSettings.serverUrl` | string | yes |  |
| `toolSettings.serverUrl` | string | yes |  |
| `toolSettings.timeout` | number | no |  |
| `toolSettings.timeout` | number | no |  |
| `type` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "async": true,
      "collectionId": "string",
      "description": "string",
      "id": "string",
      "isActive": true,
      "messages": [
        {
          "content": "string",
          "type": "string"
        }
      ],
      "name": "Ava Chen",
      "params": {
        "location": {
          "description": "string",
          "type": "string"
        }
      },
      "persistentId": "string",
      "projectId": "string",
      "toolSettings": {
        "authToken": "string",
        "httpHeaders": {
          "Authorization": "string",
          "Content-Type": "string"
        },
        "methodType": "string",
        "pathParameters": {
          "userId": "string"
        },
        "serverUrl": "https://example.com",
        "timeout": 1
      },
      "type": "string",
      "userId": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `async` | boolean |  |
| `collectionId` | string |  |
| `description` | string |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `messages[].content` | string |  |
| `messages[].type` | string |  |
| `name` | string |  |
| `params.location.description` | string |  |
| `params.location.type` | string |  |
| `persistentId` | string |  |
| `projectId` | string |  |
| `toolSettings.authToken` | string |  |
| `toolSettings.httpHeaders.Authorization` | string |  |
| `toolSettings.httpHeaders.Content-Type` | string |  |
| `toolSettings.methodType` | string |  |
| `toolSettings.pathParameters.userId` | string |  |
| `toolSettings.serverUrl` | string |  |
| `toolSettings.timeout` | number |  |
| `type` | string |  |
| `userId` | string |  |
| `version` | number |  |

## Native endpoint

Through the native Hamsa API, this operation is `POST /v2/voice-agents/web-tool` (base URL `https://api.tryhamsa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-web-tool.md) for the provider-specific parameters and requirements.

