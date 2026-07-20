# Timeular: V3 Me

Retrieves the current user from the Timeular v3 API.

```
GET https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-me
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-me?${params}`, {
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
      "data": {
        "defaultSpaceId": "string",
        "email": "ava@example.com",
        "name": "Ava Chen",
        "userId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.defaultSpaceId` | string |  |
| `data.email` | string |  |
| `data.name` | string |  |
| `data.userId` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `GET /api/v3/me` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v3-me.md) for the provider-specific parameters and requirements.

