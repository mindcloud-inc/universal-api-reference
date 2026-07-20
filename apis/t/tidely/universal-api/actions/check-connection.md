# Tidely: Check Connection



```
GET https://connect.mindcloud.co/v1/universal/tidely/latest/actions/check-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tidely/latest/actions/check-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tidely/latest/actions/check-connection?${params}`, {
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
      "name": "Ava Chen",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | Name associated with the authenticated Tidely account. |
| `success` | boolean | Whether the Tidely API key is valid. |

## Native endpoint

Through the native Tidely API, this operation is `GET /api/v1/open-api/authentication/verifyAuth` (base URL `https://api.tidely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-connection.md) for the provider-specific parameters and requirements.

