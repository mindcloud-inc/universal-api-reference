# Recallai: List Zoom OAuth Apps

Retrieves Zoom OAuth apps from Recallai.

```
GET https://connect.mindcloud.co/v1/universal/recallai/latest/actions/list-zoom-o-auth-apps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recallai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recallai/latest/actions/list-zoom-o-auth-apps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recallai/latest/actions/list-zoom-o-auth-apps?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "clientId": "string",
      "clientSecret": "string",
      "createdAt": "string",
      "id": "string",
      "kind": "string",
      "webhookLastValidation": "string",
      "webhookSecret": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | string |  |
| `clientSecret` | string |  |
| `createdAt` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `webhookLastValidation` | string |  |
| `webhookSecret` | string |  |

## Native endpoint

Through the native Recallai API, this operation is `GET /api/v2/zoom-oauth-apps/` (base URL `https://{{credentials.workspaceRegion}}.recall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-zoom-o-auth-apps.md) for the provider-specific parameters and requirements.

