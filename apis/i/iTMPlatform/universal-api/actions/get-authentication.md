# ITM Platform: Get Authentication



```
GET https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-authentication
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ITM Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-authentication?${params}`, {
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
      "result": "string",
      "resultStatus": "string",
      "token": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string | Provider-reported login result. |
| `resultStatus` | string | Provider-reported result status code. |
| `token` | string | Session token returned by the login endpoint. |
| `userId` | string | Authenticated ITM user identifier. |

## Native endpoint

Through the native ITM Platform API, this operation is `GET /login/{APIKey}` (base URL `https://api.itmplatform.com/{{credentials.company}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-authentication.md) for the provider-specific parameters and requirements.

