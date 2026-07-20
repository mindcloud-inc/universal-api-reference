# Hoops: Get User Info



```
GET https://connect.mindcloud.co/v1/universal/hoops/latest/actions/get-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hoops `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hoops/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hoops/latest/actions/get-user-info?${params}`, {
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
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Hoops API, this operation is `GET /userinfo` (base URL `https://use.hoop.dev/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-info.md) for the provider-specific parameters and requirements.

