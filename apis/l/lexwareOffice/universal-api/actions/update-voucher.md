# Lexware Office: Update Voucher

Updates an existing voucher in Lexware Office.

```
PUT https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/update-voucher
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lexware Office `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/update-voucher" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "780a9985-29a1-4daa-aa9c-196ee0dd99f5",
  "type": "purchaseinvoice",
  "taxType": "gross",
  "version": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/update-voucher', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "780a9985-29a1-4daa-aa9c-196ee0dd99f5",
    "type": "purchaseinvoice",
    "taxType": "gross",
    "version": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Voucher ID from Lexware. Example: `780a9985-29a1-4daa-aa9c-196ee0dd99f5`. |
| `type` | string | yes | Voucher type. Example: `purchaseinvoice`. |
| `voucherStatus` | string | no | Voucher status. Example: `unchecked`. |
| `voucherNumber` | string | no | Voucher number. Example: `MC-20260312-1801`. |
| `voucherDate` | date | no | Voucher date. Example: `2026-03-12`. |
| `totalGrossAmount` | number | no | Total gross amount. Example: `119`. |
| `totalTaxAmount` | number | no | Total tax amount. Example: `19`. |
| `taxType` | string | yes | Tax type. Example: `gross`. |
| `useCollectiveContact` | boolean | no | Use the collective contact. Example: `true`. |
| `contactId` | string | no | Existing contact ID. Example: `4e8a4c65-bd7e-4b4b-b4ed-1c8d6d6a6abc`. |
| `voucherItems[]` | array<object> | no | Array of voucher item objects. Example: `[object Object]`. |
| `version` | number | yes | Current voucher version from Lexware. Example: `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shippingDate` | date | no | Shipping date. Example: `2026-03-13`. |
| `dueDate` | date | no | Due date. Example: `2026-03-20`. |

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
| `resourceUri` | string | Canonical Lexware URI for the updated voucher. |
| `updatedDate` | date | Last update timestamp. |
| `version` | number | Current voucher version. |

## Native endpoint

Through the native Lexware Office API, this operation is `PUT /v1/vouchers/:id` (base URL `https://api.lexware.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-voucher.md) for the provider-specific parameters and requirements.

