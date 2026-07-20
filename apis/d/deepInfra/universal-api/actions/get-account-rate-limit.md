# Deep Infra: Get Account Rate Limit



```
GET https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-account-rate-limit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deep Infra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-account-rate-limit?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-account-rate-limit?${params}`, {
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
      "limit": 1,
      "remaining": 1,
      "requests_per_minute": 1,
      "reset": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limit` | number | Configured account rate limit. |
| `remaining` | number | Remaining requests in the current window when returned. |
| `requests_per_minute` | number | Requests-per-minute limit when returned by the provider. |
| `reset` | string | Rate limit reset time or window when returned. |

## Native endpoint

Through the native Deep Infra API, this operation is `GET /v1/me/rate_limit` (base URL `https://api.deepinfra.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-rate-limit.md) for the provider-specific parameters and requirements.

