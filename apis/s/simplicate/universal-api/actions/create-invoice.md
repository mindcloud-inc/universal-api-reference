# Simplicate: Create Invoice



```
POST https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceLines": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/create-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceLines": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `date` | string | no | Invoice date in YYYY-MM-DD format. |
| `myOrganizationProfileId` | string | no | My organization profile identifier. |
| `organizationId` | string | no | Invoice recipient organization identifier. |
| `paymentTermId` | string | no | Payment term identifier. |
| `statusId` | string | no | Invoice status identifier. |
| `subject` | string | no | Invoice subject. |
| `invoiceLines` | list<object> | yes | Array of invoice line objects. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Simplicate API, this operation is `POST /invoices/invoice` (base URL `https://{{credentials.subdomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

