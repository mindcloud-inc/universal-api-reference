# Recallai: Update Google Login Group

Updates a Google login group in Recallai.

```
PUT https://connect.mindcloud.co/v1/universal/recallai/latest/actions/update-google-login-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recallai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/recallai/latest/actions/update-google-login-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recallai/latest/actions/update-google-login-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | A UUID string identifying this google login group. |
| `loginMode` | string | no | * `always` - Always * `only_if_required` - Only If Required |
| `name` | string | no | Name of the login group. It can used to filter out login groups when retrieving them via API. |

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
        {}
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
| `logins` | array<object> |  |
| `name` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Recallai API, this operation is `PATCH /api/v2/google-login-groups/:id/` (base URL `https://{{credentials.workspaceRegion}}.recall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-google-login-group.md) for the provider-specific parameters and requirements.

