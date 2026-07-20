# Tidely: Delete Invoice



```
DELETE https://connect.mindcloud.co/v1/universal/tidely/latest/actions/delete-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/tidely/latest/actions/delete-invoice?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tidely/latest/actions/delete-invoice?${params}`, {
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
| `contactName` | string | no | Invoice contact name. |
| `invoiceId` | string | no | External invoice identifier to delete. |
| `invoiceNumber` | string | no | Invoice number. |
| `invoiceStatus` | string | no | Tidely invoice status. |
| `invoiceType` | string | no | Tidely invoice type. |
| `totalGrossAmount` | string | no | Gross invoice amount. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invoiceId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invoiceId` | string | Tidely invoice identifier. |
| `success` | boolean | Whether the invoice operation succeeded. |

## Native endpoint

Through the native Tidely API, this operation is `POST /api/v1/open-api/invoices` (base URL `https://api.tidely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-invoice.md) for the provider-specific parameters and requirements.

