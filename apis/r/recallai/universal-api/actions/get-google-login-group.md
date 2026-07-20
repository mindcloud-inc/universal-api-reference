# Recallai: Get Google Login Group

Retrieves a Google login group from Recallai.

```
GET https://connect.mindcloud.co/v1/universal/recallai/latest/actions/get-google-login-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recallai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recallai/latest/actions/get-google-login-group?connectionId=$CONNECTION_ID&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recallai/latest/actions/get-google-login-group?${params}`, {
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
| `groupId` | string | yes | A UUID string identifying this google login group. |

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

Through the native Recallai API, this operation is `GET /api/v2/google-login-groups/:id/` (base URL `https://{{credentials.workspaceRegion}}.recall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-google-login-group.md) for the provider-specific parameters and requirements.

