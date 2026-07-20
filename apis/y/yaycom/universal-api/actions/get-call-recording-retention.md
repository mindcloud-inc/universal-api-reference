# Yay.com: Get Call Recording Retention

Retrieves call recording retention from Yay.com.

```
GET https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/get-call-recording-retention
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yay.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/get-call-recording-retention?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/get-call-recording-retention?${params}`, {
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
      "expiresIn": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiresIn` | number | Call recording retention duration returned by Yay, in seconds. |

## Native endpoint

Through the native Yay.com API, this operation is `GET /voip/call-retention` (base URL `https://api.yay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call-recording-retention.md) for the provider-specific parameters and requirements.

