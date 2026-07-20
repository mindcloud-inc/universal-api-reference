# Browser Use: Get Account Billing

Retrieves account billing details from Browser Use.

```
GET https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/get-account-billing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browser Use `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/get-account-billing?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/get-account-billing?${params}`, {
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
      "additionalCreditsBalanceUsd": 1,
      "monthlyCreditsBalanceUsd": 1,
      "name": "Ava Chen",
      "planInfo": {},
      "projectId": "string",
      "rateLimit": 1,
      "totalCreditsBalanceUsd": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalCreditsBalanceUsd` | number | Additional top-up credit balance in USD |
| `monthlyCreditsBalanceUsd` | number | Monthly subscription credit balance in USD |
| `name` | string | Account user name, when available |
| `planInfo` | object | Plan information |
| `projectId` | string | Browser Use project ID |
| `rateLimit` | number | Account rate limit |
| `totalCreditsBalanceUsd` | number | Total credit balance in USD |

## Native endpoint

Through the native Browser Use API, this operation is `GET /billing/account` (base URL `https://api.browser-use.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-billing.md) for the provider-specific parameters and requirements.

