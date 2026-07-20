# Merit: List Vendors



```
GET https://connect.mindcloud.co/v1/universal/merit/latest/actions/list-vendors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/merit/latest/actions/list-vendors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/merit/latest/actions/list-vendors?${params}`, {
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
| `id` | string | no | Vendor GUID. If provided, other selectors are ignored. Example: `1b10589a-a17b-4325-5ba1-08de9fd83d3e`. |
| `name` | string | no | Broad vendor name match. Example: `MindCloud Test Vendor`. |
| `regNo` | string | no | Exact vendor registration number match. |
| `vatRegNo` | string | no | Exact vendor VAT registration number match. |
| `changedDate` | string | no | Date of changed or created vendor in YYYYmmDD format. Example: `20260422`. |
| `withComments` | boolean | no | Whether to include comments. |
| `commentsFrom` | date | no | Only comments later than this date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "changedDate": "2026-05-07T12:00:00.000Z",
      "countryCode": "string",
      "countryName": "Ava Chen",
      "currencyCode": "string",
      "email": "ava@example.com",
      "name": "Ava Chen",
      "overdueCharge": 1,
      "paymentDeadLine": 1,
      "phoneNo": "string",
      "referenceNo": "string",
      "vatAccountable": true,
      "vendorId": "string",
      "vendorType": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changedDate` | date | Changed date. |
| `countryCode` | string | Country code. |
| `countryName` | string | Country name. |
| `currencyCode` | string | Currency code. |
| `email` | string | Vendor email. |
| `name` | string | Vendor name. |
| `overdueCharge` | number | Overdue charge. |
| `paymentDeadLine` | number | Default payment deadline in days. |
| `phoneNo` | string | Primary phone number. |
| `referenceNo` | string | Reference number. |
| `vatAccountable` | boolean | Whether the vendor is VAT accountable. |
| `vendorId` | string | Vendor ID. |
| `vendorType` | number | Vendor type. |

## Native endpoint

Through the native Merit API, this operation is `POST v1/getvendors` (base URL `https://aktiva.merit.ee/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vendors.md) for the provider-specific parameters and requirements.

