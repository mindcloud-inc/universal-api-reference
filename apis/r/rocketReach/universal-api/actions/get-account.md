# RocketReach: Get Account

Retrieves account details from RocketReach.

```
GET https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RocketReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/get-account?${params}`, {
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
      "creditUsage": [
        {
          "allocated": 1,
          "creditType": "string",
          "remaining": 1,
          "used": 1
        }
      ],
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "rateLimits": [
        {
          "action": "string",
          "duration": "string",
          "limit": 1,
          "remaining": 1,
          "used": 1
        }
      ],
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditUsage[].allocated` | number |  |
| `creditUsage[].creditType` | string |  |
| `creditUsage[].remaining` | number |  |
| `creditUsage[].used` | number |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `rateLimits[].action` | string |  |
| `rateLimits[].duration` | string |  |
| `rateLimits[].limit` | number |  |
| `rateLimits[].remaining` | number |  |
| `rateLimits[].used` | number |  |
| `state` | string |  |

## Native endpoint

Through the native RocketReach API, this operation is `GET /account/` (base URL `https://api.rocketreach.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

