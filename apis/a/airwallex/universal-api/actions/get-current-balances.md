# Airwallex: Get Current Balances

Retrieves current balances for a connected Airwallex account.

```
GET https://connect.mindcloud.co/v1/universal/airwallex/latest/actions/get-current-balances
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airwallex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airwallex/latest/actions/get-current-balances?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airwallex/latest/actions/get-current-balances?${params}`, {
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
      "accountType": "string",
      "availableAmount": 1,
      "currency": "string",
      "pendingAmount": 1,
      "prepaymentAmount": 1,
      "reservedAmount": 1,
      "totalAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountType` | string | Balance account type, such as cash. |
| `availableAmount` | number | Currently available balance amount. |
| `currency` | string | Balance currency code. |
| `pendingAmount` | number | Pending balance amount. |
| `prepaymentAmount` | number | Prepayment balance amount. |
| `reservedAmount` | number | Reserved balance amount. |
| `totalAmount` | number | Total balance amount. |

## Native endpoint

Through the native Airwallex API, this operation is `GET /api/v1/balances/current` (base URL `https://api-demo.airwallex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-balances.md) for the provider-specific parameters and requirements.

