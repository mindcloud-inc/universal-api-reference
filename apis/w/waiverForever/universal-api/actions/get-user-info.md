# WaiverForever: Get User Info

Retrieves user info from WaiverForever.

```
GET https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/get-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverForever `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/get-user-info?${params}`, {
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
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `username` | string | WaiverForever account username. |

## Native endpoint

Through the native WaiverForever API, this operation is `GET /openapi/v1/auth/userInfo` (base URL `https://api.waiverforever.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-info.md) for the provider-specific parameters and requirements.

