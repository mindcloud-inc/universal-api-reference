# v0: Get Plan

Retrieves the current plan from v0.

```
GET https://connect.mindcloud.co/v1/universal/v0/latest/actions/get-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a v0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/v0/latest/actions/get-plan?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/v0/latest/actions/get-plan?${params}`, {
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
      "balance": {
        "remaining": 1,
        "total": 1
      },
      "billingCycle": {
        "end": 1,
        "start": 1
      },
      "object": "string",
      "plan": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance.remaining` | number |  |
| `balance.total` | number |  |
| `billingCycle.end` | number |  |
| `billingCycle.start` | number |  |
| `object` | string |  |
| `plan` | string |  |

## Native endpoint

Through the native v0 API, this operation is `GET /v1/user/plan` (base URL `https://api.v0.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-plan.md) for the provider-specific parameters and requirements.

