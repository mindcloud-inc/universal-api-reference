# Orshot: Get Profile and Workspaces



```
GET https://connect.mindcloud.co/v1/universal/orshot/latest/actions/get-profile-and-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orshot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orshot/latest/actions/get-profile-and-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orshot/latest/actions/get-profile-and-workspaces?${params}`, {
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
      "email": "ava@example.com",
      "name": "Ava Chen",
      "user_id": "string",
      "workspaces": [
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
| `email` | string | Email address for the authenticated user. |
| `name` | string | Display name for the authenticated user or workspace owner. |
| `user_id` | string | Unique identifier for the authenticated Orshot user. |
| `workspaces` | array<object> | Workspaces available to the authenticated user. |

## Native endpoint

Through the native Orshot API, this operation is `GET /me` (base URL `https://api.orshot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-profile-and-workspaces.md) for the provider-specific parameters and requirements.

