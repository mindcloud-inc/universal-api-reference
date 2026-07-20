# Dash.app: Create Saved Search

Creates a new saved search in Dash.app.

```
POST https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/create-saved-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dash.app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/create-saved-search" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "criterion": "[object Object]",
  "emailUserOnNewUploads": "false",
  "name": "Ava Chen",
  "sorts[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/create-saved-search', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "criterion": "[object Object]",
    "emailUserOnNewUploads": "false",
    "name": "Ava Chen",
    "sorts[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `criterion` | object | yes | Dash criterion object Example: `[object Object]`. |
| `emailUserOnNewUploads` | boolean | yes | Whether to email the user when new uploads match Default: `false`. |
| `name` | string | yes | Saved search name |
| `sorts[]` | array<object> | yes | Dash sorts array Example: `[object Object]`. |

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

Through the native Dash.app API, this operation is `POST /saved-searches` (base URL `https://api-v2.dash.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-saved-search.md) for the provider-specific parameters and requirements.

