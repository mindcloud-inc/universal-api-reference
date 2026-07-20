# Lexware Office: List Voucher Metadata

Retrieves and filters voucher metadata in Lexware Office.

```
GET https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/list-voucher-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lexware Office `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/list-voucher-metadata?connectionId=$CONNECTION_ID&limit=25&offset=0&voucherType=any&voucherStatus=any" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "voucherType": "any",
  "voucherStatus": "any"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/list-voucher-metadata?${params}`, {
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
| `voucherType` | string | yes | Comma-separated voucher types or any. Default: `any`. Example: `any`. |
| `voucherStatus` | string | yes | Comma-separated voucher statuses or any. Default: `any`. Example: `any`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `archived` | boolean | no | Filter archived vouchers. Example: `false`. |
| `contactId` | string | no | Existing Lexware contact ID. Example: `4e8a4c65-bd7e-4b4b-b4ed-1c8d6d6a6abc`. |
| `voucherDateFrom` | date | no | Filter by voucher date from yyyy-MM-dd. Example: `2026-03-01`. |
| `voucherDateTo` | date | no | Filter by voucher date to yyyy-MM-dd. Example: `2026-03-31`. |
| `createdDateFrom` | date | no | Filter by created date from yyyy-MM-dd. Example: `2026-03-01`. |
| `createdDateTo` | date | no | Filter by created date to yyyy-MM-dd. Example: `2026-03-31`. |
| `updatedDateFrom` | date | no | Filter by updated date from yyyy-MM-dd. Example: `2026-03-01`. |
| `updatedDateTo` | date | no | Filter by updated date to yyyy-MM-dd. Example: `2026-03-31`. |
| `voucherNumber` | string | no | Exact voucher number filter. Example: `RE-2026-0001`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "contactName": "Ava Chen",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "openAmount": 1,
      "totalAmount": 1,
      "updatedDate": "2026-05-07T12:00:00.000Z",
      "voucherDate": "2026-05-07T12:00:00.000Z",
      "voucherNumber": "string",
      "voucherStatus": "string",
      "voucherType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `contactName` | string |  |
| `createdDate` | date |  |
| `currency` | string |  |
| `dueDate` | date |  |
| `id` | string |  |
| `openAmount` | number |  |
| `totalAmount` | number |  |
| `updatedDate` | date |  |
| `voucherDate` | date |  |
| `voucherNumber` | string |  |
| `voucherStatus` | string |  |
| `voucherType` | string |  |

## Native endpoint

Through the native Lexware Office API, this operation is `GET /v1/voucherlist` (base URL `https://api.lexware.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-voucher-metadata.md) for the provider-specific parameters and requirements.

