# TPSCheck: Get credits



```
GET https://connect.mindcloud.co/v1/universal/tPSCheck/latest/actions/get-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TPSCheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tPSCheck/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tPSCheck/latest/actions/get-credits?${params}`, {
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
      "monthlyLimit": 1,
      "plan": "string",
      "requestsRemaining": 1,
      "requestsUsed": 1,
      "resetDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `monthlyLimit` | number | Total requests allowed this billing period. |
| `plan` | string | Current subscription plan name. |
| `requestsRemaining` | number | Number of requests still available this period. |
| `requestsUsed` | number | Number of API requests made this billing period. |
| `resetDate` | date | When usage resets in ISO 8601 format. |

## Native endpoint

Through the native TPSCheck API, this operation is `GET /credits` (base URL `https://api.tpscheck.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credits.md) for the provider-specific parameters and requirements.

