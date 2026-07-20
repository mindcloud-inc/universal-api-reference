# Whattime: Get My User



```
GET https://connect.mindcloud.co/v1/universal/whattime/latest/actions/get-my-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whattime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whattime/latest/actions/get-my-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whattime/latest/actions/get-my-user?${params}`, {
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
      "code": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "name": "Ava Chen",
      "organization": {
        "code": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "uri": "string"
      },
      "role": "string",
      "slug": "string",
      "time_zone": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `created_at` | date |  |
| `email` | string |  |
| `name` | string |  |
| `organization` | object |  |
| `organization.code` | string |  |
| `organization.created_at` | date |  |
| `organization.name` | string |  |
| `organization.updated_at` | date |  |
| `organization.uri` | string |  |
| `role` | string |  |
| `slug` | string |  |
| `time_zone` | string |  |
| `updated_at` | date |  |
| `uri` | string |  |

## Native endpoint

Through the native Whattime API, this operation is `GET /users/me` (base URL `https://api.whattime.co.kr/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-user.md) for the provider-specific parameters and requirements.

