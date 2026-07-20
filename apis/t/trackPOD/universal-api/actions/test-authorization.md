# Track-POD: Test Authorization

Retrieves authorization and rate limit status from Track-POD.

```
GET https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/test-authorization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Track-POD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/test-authorization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/test-authorization?${params}`, {
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Track-POD returns ok when the API key is valid and the request is within rate limits. |

## Native endpoint

Through the native Track-POD API, this operation is `GET /Test` (base URL `https://api.track-pod.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/test-authorization.md) for the provider-specific parameters and requirements.

