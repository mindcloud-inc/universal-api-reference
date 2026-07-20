# Pinboard: Get User Secret



```
GET https://connect.mindcloud.co/v1/universal/pinboard/latest/actions/get-user-secret
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinboard/latest/actions/get-user-secret?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinboard/latest/actions/get-user-secret?${params}`, {
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
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string | The user's private RSS secret. |

## Native endpoint

Through the native Pinboard API, this operation is `GET /user/secret` (base URL `https://api.pinboard.in/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-secret.md) for the provider-specific parameters and requirements.

