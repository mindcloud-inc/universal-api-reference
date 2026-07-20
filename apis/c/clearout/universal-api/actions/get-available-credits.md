# Clearout: Get Available Credits

Retrieves available credits from your Clearout account.

```
GET https://connect.mindcloud.co/v1/universal/clearout/latest/actions/get-available-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clearout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clearout/latest/actions/get-available-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clearout/latest/actions/get-available-credits?${params}`, {
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
      "availableCredits": 1,
      "credits": {
        "available": 1,
        "availableDailyVerifyLimit": "string",
        "resetDailyVerifyLimitDate": "string",
        "subs": "string",
        "total": 1
      },
      "lowCreditBalanceMinThreshold": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableCredits` | number |  |
| `credits` | object |  |
| `credits.available` | number |  |
| `credits.availableDailyVerifyLimit` | string |  |
| `credits.resetDailyVerifyLimitDate` | string |  |
| `credits.subs` | string |  |
| `credits.total` | number |  |
| `lowCreditBalanceMinThreshold` | number |  |

## Native endpoint

Through the native Clearout API, this operation is `GET /email_verify/getcredits` (base URL `https://api.clearout.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-available-credits.md) for the provider-specific parameters and requirements.

