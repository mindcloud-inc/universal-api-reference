# Recallai: Create Google Login Group

Creates a new Google login group in Recallai.

```
POST https://connect.mindcloud.co/v1/universal/recallai/latest/actions/create-google-login-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recallai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recallai/latest/actions/create-google-login-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "loginMode": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recallai/latest/actions/create-google-login-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "loginMode": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `loginMode` | string | yes | * `always` - Always * `only_if_required` - Only If Required |
| `name` | string | yes | Name of the login group. It can used to filter out login groups when retrieving them via API. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "loginMode": "string",
      "logins": [
        "string"
      ],
      "name": "Ava Chen",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | string |  |
| `loginMode` | string |  |
| `logins` | array |  |
| `name` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Recallai API, this operation is `POST /api/v2/google-login-groups/` (base URL `https://{{credentials.workspaceRegion}}.recall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-google-login-group.md) for the provider-specific parameters and requirements.

