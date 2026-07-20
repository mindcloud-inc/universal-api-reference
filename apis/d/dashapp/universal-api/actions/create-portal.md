# Dash.app: Create Portal

Creates a new portal in Dash.app.

```
POST https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/create-portal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dash.app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/create-portal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "showRecentlyAddedAssets": "true",
  "slug": "string",
  "welcomeMessage": "[object Object]",
  "whitelistedFolderFieldOptionIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/create-portal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "showRecentlyAddedAssets": "true",
    "slug": "string",
    "welcomeMessage": "[object Object]",
    "whitelistedFolderFieldOptionIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assetPermittedActions` | string | no | Portal asset permission mode Default: `VIEW`. |
| `name` | string | yes | Portal name |
| `showRecentlyAddedAssets` | boolean | yes | Whether to show recently added assets Default: `true`. |
| `slug` | string | yes | Portal slug |
| `welcomeMessage` | object | yes | Portal welcome message object Example: `[object Object]`. |
| `whitelistedFolderFieldOptionIds[]` | array<string> | yes | Folder field option IDs available in the portal |

## Response

```json
{
  "success": true,
  "data": [
    {
      "permittedActions": [
        {}
      ],
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `permittedActions` | array<object> |  |
| `result` | object |  |

## Native endpoint

Through the native Dash.app API, this operation is `POST /portals` (base URL `https://api-v2.dash.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-portal.md) for the provider-specific parameters and requirements.

