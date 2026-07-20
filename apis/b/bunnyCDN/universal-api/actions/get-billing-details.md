# BunnyCDN: Get Billing Details

Retrieves detailed billing information from BunnyCDN.

```
GET https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/get-billing-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BunnyCDN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/get-billing-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/get-billing-details?${params}`, {
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
      "Balance": 1,
      "BillingEnabled": true,
      "BillingRecords": [
        {}
      ],
      "SavedPaymentMethods": [
        {}
      ],
      "ThisMonthCharges": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Balance` | number |  |
| `BillingEnabled` | boolean |  |
| `BillingRecords` | array<object> |  |
| `SavedPaymentMethods` | array<object> |  |
| `ThisMonthCharges` | number |  |

## Native endpoint

Through the native BunnyCDN API, this operation is `GET /billing` (base URL `https://api.bunny.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-billing-details.md) for the provider-specific parameters and requirements.

