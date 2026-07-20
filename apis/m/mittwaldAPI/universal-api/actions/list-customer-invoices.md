# mittwald: List Customer Invoices

Retrieves customer invoices from mittwald API.

```
GET https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/list-customer-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mittwald `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/list-customer-invoices?connectionId=$CONNECTION_ID&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/list-customer-invoices?${params}`, {
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
| `customerId` | string | yes | The unique identifier of the customer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerId": "string",
      "date": "string",
      "id": "string",
      "invoiceNumber": "string",
      "status": "string",
      "totalGross": 1,
      "totalNet": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerId` | string |  |
| `date` | string |  |
| `id` | string |  |
| `invoiceNumber` | string |  |
| `status` | string |  |
| `totalGross` | number |  |
| `totalNet` | number |  |

## Native endpoint

Through the native mittwald API, this operation is `GET /v2/customers/:customerId/invoices` (base URL `https://api.mittwald.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-invoices.md) for the provider-specific parameters and requirements.

