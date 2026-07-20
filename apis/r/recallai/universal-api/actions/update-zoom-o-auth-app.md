# Recallai: Update Zoom OAuth App

Updates an existing Zoom OAuth app in Recallai.

```
PUT https://connect.mindcloud.co/v1/universal/recallai/latest/actions/update-zoom-o-auth-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recallai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/recallai/latest/actions/update-zoom-o-auth-app" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "zoomOauthAppId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recallai/latest/actions/update-zoom-o-auth-app', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "zoomOauthAppId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientSecret` | string | no | Client Secret |
| `webhookSecret` | string | no | Webhook Secret |
| `zoomOauthAppId` | string | yes | A UUID string identifying this zoom o auth app. |

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

Through the native Recallai API, this operation is `PATCH /api/v2/zoom-oauth-apps/:id/` (base URL `https://{{credentials.workspaceRegion}}.recall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-zoom-o-auth-app.md) for the provider-specific parameters and requirements.

