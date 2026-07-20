# Survalyzer: Update WebHook



```
PUT https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/update-web-hook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Survalyzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/update-web-hook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webHookId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/update-web-hook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webHookId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webHookId` | string | yes |  |
| `eventType` | string | no |  |
| `entityIdentifier` | string | no |  |
| `securityToken` | string | no |  |
| `webHookUrl` | string | no |  |
| `workspaceId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorCode": "string",
      "errorMessage": "string",
      "isSuccess": true
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

## Native endpoint

Through the native Survalyzer API, this operation is `POST /publicapi/WebHook/v3/UpdateWebHook` (base URL `https://api.survalyzer-eu.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-web-hook.md) for the provider-specific parameters and requirements.

