# Lexware Office: Create Voucher

Creates a new voucher in Lexware Office.

```
POST https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/create-voucher
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lexware Office `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/create-voucher" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "expenseinvoice",
  "taxType": "gross"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/create-voucher', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "expenseinvoice",
    "taxType": "gross"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Voucher type, for example expenseinvoice or salesinvoice. Example: `expenseinvoice`. |
| `voucherStatus` | string | no | Set unchecked for draft bookkeeping vouchers. Default: `unchecked`. Example: `unchecked`. |
| `voucherNumber` | string | no | Voucher number; required unless status is unchecked. Example: `RE-2026-0001`. |
| `voucherDate` | date | no | Voucher date in RFC 3339 format. Example: `2026-03-12T00:00:00.000+01:00`. |
| `totalGrossAmount` | number | no | Total gross amount; required unless status is unchecked. Example: `119`. |
| `totalTaxAmount` | number | no | Total tax amount; required unless status is unchecked. Example: `19`. |
| `taxType` | string | yes | Tax type, for example gross or net. Default: `gross`. Example: `gross`. |
| `useCollectiveContact` | boolean | no | Use the Lexware collective contact instead of contactId. Example: `true`. |
| `contactId` | string | no | Existing contact ID when not using the collective contact. Example: `4e8a4c65-bd7e-4b4b-b4ed-1c8d6d6a6abc`. |
| `voucherItems[]` | array<object> | no | Array of voucher item objects. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shippingDate` | date | no | Optional shipping date in RFC 3339 format. Example: `2026-03-13T00:00:00.000+01:00`. |
| `dueDate` | date | no | Optional due date in RFC 3339 format. Example: `2026-03-20T00:00:00.000+01:00`. |
| `version` | number | no | Optional version on create; must be 1 if provided. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "resourceUri": "string",
      "updatedDate": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDate` | date | Creation timestamp. |
| `id` | string | Voucher ID. |
| `resourceUri` | string | Canonical Lexware URI for the created voucher. |
| `updatedDate` | date | Last update timestamp. |
| `version` | number | Current voucher version. |

## Native endpoint

Through the native Lexware Office API, this operation is `POST /v1/vouchers` (base URL `https://api.lexware.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-voucher.md) for the provider-specific parameters and requirements.

