# Pilvio: List Billing Accounts



```
GET https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-billing-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pilvio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-billing-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-billing-accounts?${params}`, {
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
      "additionalData": "string",
      "addressLine1": "string",
      "allowDebt": true,
      "canPay": true,
      "city": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalData` | string |  |
| `addressLine1` | string |  |
| `allowDebt` | boolean |  |
| `canPay` | boolean |  |
| `city` | string |  |

## Native endpoint

Through the native Pilvio API, this operation is `GET /payment/billing_account/list` (base URL `https://api.pilvio.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-billing-accounts.md) for the provider-specific parameters and requirements.

