# Recallai: Create Zoom OAuth App

Creates a new Zoom OAuth app in Recallai.

```
POST https://connect.mindcloud.co/v1/universal/recallai/latest/actions/create-zoom-o-auth-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recallai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recallai/latest/actions/create-zoom-o-auth-app" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": "string",
  "clientSecret": "string",
  "kind": "string",
  "webhookSecret": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recallai/latest/actions/create-zoom-o-auth-app', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": "string",
    "clientSecret": "string",
    "kind": "string",
    "webhookSecret": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | string | yes | Client ID |
| `clientSecret` | string | yes | Client Secret |
| `kind` | string | yes | * `user_level` - User Level * `account_level` - Account Level |
| `webhookSecret` | string | yes | Webhook Secret |

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

Through the native Recallai API, this operation is `POST /api/v2/zoom-oauth-apps/` (base URL `https://{{credentials.workspaceRegion}}.recall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-zoom-o-auth-app.md) for the provider-specific parameters and requirements.

