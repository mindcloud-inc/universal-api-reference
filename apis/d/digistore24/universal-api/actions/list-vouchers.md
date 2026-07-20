# Digistore24: List Vouchers

Retrieves a list of voucher codes from Digistore24.

```
GET https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/list-vouchers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digistore24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/list-vouchers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/list-vouchers?${params}`, {
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
      "code": "string",
      "countLeft": 1,
      "currency": "string",
      "expiresAt": "string",
      "firstAmount": 1,
      "firstRate": 1,
      "id": 1,
      "isCountLimited": "string",
      "isDiscardingEarlyBird": "string",
      "otherAmounts": 1,
      "otherRates": 1,
      "productIds": "string",
      "upgradePolicy": "string",
      "validUntil": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Voucher code |
| `countLeft` | number | Remaining usage count |
| `currency` | string | Currency code |
| `expiresAt` | string | Expiration date |
| `firstAmount` | number | Discount amount for first payment |
| `firstRate` | number | Discount rate for first payment |
| `id` | number | Voucher ID |
| `isCountLimited` | string | Whether voucher usage is limited |
| `isDiscardingEarlyBird` | string | Whether early bird discount is discarded |
| `otherAmounts` | number | Discount amount for subsequent payments |
| `otherRates` | number | Discount rate for subsequent payments |
| `productIds` | string | Applicable product IDs or all |
| `upgradePolicy` | string | Upgrade policy |
| `validUntil` | string | Validity end date |

## Native endpoint

Through the native Digistore24 API, this operation is `POST /listVouchers` (base URL `https://www.digistore24.com/api/call`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vouchers.md) for the provider-specific parameters and requirements.

