# Lexware Office: Retrieve Voucher

Retrieves a voucher from Lexware Office.

```
GET https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/retrieve-voucher
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lexware Office `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/retrieve-voucher?connectionId=$CONNECTION_ID&id=780a9985-29a1-4daa-aa9c-196ee0dd99f5" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "780a9985-29a1-4daa-aa9c-196ee0dd99f5"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/retrieve-voucher?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Voucher ID from Lexware. Example: `780a9985-29a1-4daa-aa9c-196ee0dd99f5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactName": "Ava Chen",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "files": [
        "string"
      ],
      "id": "string",
      "organizationId": "string",
      "taxType": "string",
      "totalGrossAmount": 1,
      "totalTaxAmount": 1,
      "type": "string",
      "updatedDate": "2026-05-07T12:00:00.000Z",
      "useCollectiveContact": true,
      "version": 1,
      "voucherDate": "2026-05-07T12:00:00.000Z",
      "voucherItems": [
        {}
      ],
      "voucherNumber": "string",
      "voucherStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactName` | string | Resolved contact name. |
| `createdDate` | date | Creation timestamp. |
| `dueDate` | date | Voucher due date. |
| `files` | array<string> | Attached file IDs. |
| `id` | string | Voucher ID. |
| `organizationId` | string | Organization ID. |
| `taxType` | string | Tax type. |
| `totalGrossAmount` | number | Total gross amount. |
| `totalTaxAmount` | number | Total tax amount. |
| `type` | string | Voucher type. |
| `updatedDate` | date | Last update timestamp. |
| `useCollectiveContact` | boolean | Whether the collective contact is used. |
| `version` | number | Current voucher version. |
| `voucherDate` | date | Voucher date. |
| `voucherItems` | array<object> | Voucher line items. |
| `voucherNumber` | string | Voucher number. |
| `voucherStatus` | string | Voucher status. |

## Native endpoint

Through the native Lexware Office API, this operation is `GET /v1/vouchers/:id` (base URL `https://api.lexware.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-voucher.md) for the provider-specific parameters and requirements.

