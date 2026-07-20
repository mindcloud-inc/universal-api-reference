# Digistore24: List Payouts

Retrieves payout credit notes from Digistore24.

```
GET https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/list-payouts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digistore24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/list-payouts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/list-payouts?${params}`, {
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
      "affiliateGrossAmount": 1,
      "affiliateNetAmount": 1,
      "affiliateVatAmount": 1,
      "commissionListUrl": "https://example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creditNoteUrl": "https://example.com",
      "currency": "string",
      "feeAmount": 1,
      "feeVatAmount": 1,
      "id": 1,
      "payoutMethod": "string",
      "processedAt": "2026-05-07T12:00:00.000Z",
      "resellerId": 1,
      "resellerName": "Ava Chen",
      "vatRate": 1,
      "vatRegulation": "string",
      "vendorGrossAmount": 1,
      "vendorNetAmount": 1,
      "vendorVatAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliateGrossAmount` | number | Affiliate gross amount |
| `affiliateNetAmount` | number | Affiliate net amount |
| `affiliateVatAmount` | number | Affiliate VAT amount |
| `commissionListUrl` | string | Commission list URL |
| `createdAt` | date | Creation timestamp |
| `creditNoteUrl` | string | Credit note URL |
| `currency` | string | Currency code |
| `feeAmount` | number | Fee amount |
| `feeVatAmount` | number | Fee VAT amount |
| `id` | number | Payout ID |
| `payoutMethod` | string | Payout method |
| `processedAt` | date | Processing timestamp |
| `resellerId` | number | Reseller ID |
| `resellerName` | string | Reseller name |
| `vatRate` | number | VAT rate |
| `vatRegulation` | string | VAT regulation |
| `vendorGrossAmount` | number | Vendor gross amount |
| `vendorNetAmount` | number | Vendor net amount |
| `vendorVatAmount` | number | Vendor VAT amount |

## Native endpoint

Through the native Digistore24 API, this operation is `GET /listPayouts` (base URL `https://www.digistore24.com/api/call`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payouts.md) for the provider-specific parameters and requirements.

