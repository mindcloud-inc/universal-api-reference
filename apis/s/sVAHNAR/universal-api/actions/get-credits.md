# SVAHNAR: Get Credits



```
GET https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/get-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SVAHNAR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/get-credits?${params}`, {
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
      "credits_remaining": 1,
      "request_metadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits_remaining` | number | Number of credits remaining for the organization. |
| `request_metadata` | object | Response metadata including the request ID. |

## Native endpoint

Through the native SVAHNAR API, this operation is `GET /v1/credits/get` (base URL `https://api.svahnar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credits.md) for the provider-specific parameters and requirements.

