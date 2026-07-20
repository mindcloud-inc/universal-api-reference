# Survalyzer: List WebHooks



```
GET https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/list-web-hooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Survalyzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/list-web-hooks?connectionId=$CONNECTION_ID&entityIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entityIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/list-web-hooks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventType` | string | no | Optional webhook event type to filter by. |
| `entityIdentifier` | string | yes | Entity identifier for the webhook subscription, or * for all. |
| `workspaceId` | number | no | Workspace identifier that owns the webhooks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorCode": "string",
      "errorMessage": "string",
      "isSuccess": true,
      "totalCount": 1,
      "webHooks": [
        {}
      ]
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
| `totalCount` | number |  |
| `webHooks` | array<object> |  |

## Native endpoint

Through the native Survalyzer API, this operation is `POST /publicapi/WebHook/v3/ReadWebHookList` (base URL `https://api.survalyzer-eu.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-web-hooks.md) for the provider-specific parameters and requirements.

