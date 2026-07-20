# ReputationLync: Add Customer

Creates a new customer in ReputationLync.

```
POST https://connect.mindcloud.co/v1/universal/reputationLync/latest/actions/add-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReputationLync `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/reputationLync/latest/actions/add-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerName": "Jane Doe"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reputationLync/latest/actions/add-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerName": "Jane Doe"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerName` | string | yes | Name of the customer to add. Example: `Jane Doe`. |
| `emailId` | string | no | Customer email address. Provide this or Phone Number. Example: `jane.doe@example.com`. |
| `phoneNumber` | string | no | Customer phone number. Provide this or Email ID. Example: `855-555-1234`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `whatsappEnabled` | string | no | Use 1 if the phone number is WhatsApp-enabled, otherwise 0. Example: `1`. |
| `tags` | string | no | Comma-separated tags to associate with the customer. Example: `retail,online`. |
| `language` | string | no | Language configured in ReputationLync for this customer. Example: `English`. |
| `source` | string | no | Source label for this customer creation. Default: `API`. Example: `API`. |
| `sourceXrefId` | string | no | External customer or transaction ID from the source system. Example: `order-1001`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerDatesNotes": "string",
      "customerId": 1,
      "result": "string",
      "skipRatingRequest": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerDatesNotes` | string | Provider notes related to customer date handling. |
| `customerId` | number | Customer identifier created by ReputationLync. |
| `result` | string | Result message returned by ReputationLync. |
| `skipRatingRequest` | boolean | Whether the provider skipped the rating request flow for the new customer. |
| `status` | string | Provider status for the add-customer request. |

## Native endpoint

Through the native ReputationLync API, this operation is `POST /addCustomer` (base URL `https://reputationlync.com/app/api/customer`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-customer.md) for the provider-specific parameters and requirements.

