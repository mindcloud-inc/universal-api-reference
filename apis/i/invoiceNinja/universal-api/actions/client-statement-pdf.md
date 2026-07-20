# Invoice Ninja: Client Statement PDF



```
GET https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/client-statement-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/client-statement-pdf?connectionId=$CONNECTION_ID&startDate=2026-01-01&endDate=2026-03-20&clientId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "2026-01-01",
  "endDate": "2026-03-20",
  "clientId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/client-statement-pdf?${params}`, {
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
| `startDate` | string | yes | Start date for the statement period in Y-m-d format. Example: `2026-01-01`. |
| `endDate` | string | yes | End date for the statement period in Y-m-d format. Example: `2026-03-20`. |
| `clientId` | string | yes | Hashed client ID for the statement. |
| `showPaymentsTable` | boolean | no | Whether to include the payments table in the PDF. |
| `showCreditsTable` | boolean | no | Whether to include the credits table in the PDF. |
| `showAgingTable` | boolean | no | Whether to include the aging table in the PDF. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Raw PDF payload returned by Invoice Ninja for the generated client statement. |

## Native endpoint

Through the native Invoice Ninja API, this operation is `POST /client_statement` (base URL `https://invoicing.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/client-statement-pdf.md) for the provider-specific parameters and requirements.

