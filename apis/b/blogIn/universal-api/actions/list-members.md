# BlogIn: List Members

Retrieves all members from BlogIn.

```
GET https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/list-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlogIn `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/list-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/list-members?${params}`, {
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
      "access_level": "string",
      "avatar": "string",
      "email": "ava@example.com",
      "id": 1,
      "job_title": "string",
      "name": "Ava Chen",
      "phone": "string",
      "status": "string",
      "surname": "Ava Chen",
      "teams": [
        {}
      ],
      "time_registered": "string",
      "timezone": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_level` | string |  |
| `avatar` | string |  |
| `email` | string |  |
| `id` | number |  |
| `job_title` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `status` | string |  |
| `surname` | string |  |
| `teams` | array<object> |  |
| `time_registered` | string |  |
| `timezone` | string |  |
| `username` | string |  |

## Native endpoint

Through the native BlogIn API, this operation is `GET /members` (base URL `https://blogin.co/api/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-members.md) for the provider-specific parameters and requirements.

