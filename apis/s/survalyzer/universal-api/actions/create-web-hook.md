# Survalyzer: Create WebHook



```
POST https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/create-web-hook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Survalyzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/create-web-hook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entityIdentifier": "string",
  "webHookUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/create-web-hook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entityIdentifier": "string",
    "webHookUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventType` | string | no |  |
| `entityIdentifier` | string | yes |  |
| `securityToken` | string | no |  |
| `webHookUrl` | string | yes |  |
| `workspaceId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorCode": "string",
      "errorMessage": "string",
      "isSuccess": true,
      "webHookId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorCode` | string |  |
| `errorMessage` | string |  |
| `isSuccess` | boolean |  |
| `webHookId` | string | Unique identifier of the created web hook. |

## Native endpoint

Through the native Survalyzer API, this operation is `POST /publicapi/WebHook/v3/CreateWebHook` (base URL `https://api.survalyzer-eu.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-web-hook.md) for the provider-specific parameters and requirements.

