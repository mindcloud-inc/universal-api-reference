# Starfish: Get Current User

Retrieves the current authenticated user from Starfish.

```
GET https://connect.mindcloud.co/v1/universal/starfish/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starfish `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starfish/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starfish/latest/actions/get-current-user?${params}`, {
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
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "id": 1,
      "meta": {},
      "rights": [
        "string"
      ],
      "status": 1,
      "type": "string",
      "userRegistered": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string |  |
| `email` | string |  |
| `id` | number |  |
| `meta` | object |  |
| `rights` | array<string> |  |
| `status` | number |  |
| `type` | string |  |
| `userRegistered` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Starfish API, this operation is `GET /users/me` (base URL `https://api.camping.care/v21`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

