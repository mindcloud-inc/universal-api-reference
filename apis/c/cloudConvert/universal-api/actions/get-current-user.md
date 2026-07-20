# CloudConvert: Get Current User

Retrieves the current user from CloudConvert.

```
GET https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudConvert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/get-current-user?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "credits": 1,
      "email": "ava@example.com",
      "id": 1,
      "links": {
        "self": "https://example.com"
      },
      "paying": true,
      "taskRegion": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `credits` | number |  |
| `email` | string |  |
| `id` | number |  |
| `links.self` | string |  |
| `paying` | boolean |  |
| `taskRegion` | string |  |
| `username` | string |  |

## Native endpoint

Through the native CloudConvert API, this operation is `GET /users/me` (base URL `https://api.cloudconvert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

