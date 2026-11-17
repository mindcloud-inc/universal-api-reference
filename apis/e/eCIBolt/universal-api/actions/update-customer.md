# ECI Bolt: Update Customer



```
PUT https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECI Bolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "etag": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "etag": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Id of the customer. |
| `etag` | string | yes | Use the etag returned by a fresh Get request to avoid overwriting a newer record. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer` | object | no |  |
| `customer.name` | string | no |  |
| `customer.status` | string | no |  |
| `customer.phone` | string | no |  |
| `customer.email` | string | no |  |
| `customer.notes` | string | no |  |
| `customer.poRequired` | boolean | no |  |
| `customer.workOrderNotes` | string | no |  |
| `customer.emailConfirmationToSupervisor` | boolean | no |  |
| `customer.optOutEmailConfirmation` | boolean | no |  |
| `customer.optOutAutoConfirmation` | boolean | no |  |
| `customer.externalId` | string | no |  |
| `customer.corporateAddress` | object | no |  |
| `customer.corporateAddress.line1` | string | no |  |
| `customer.corporateAddress.line2` | string | no |  |
| `customer.corporateAddress.city` | string | no |  |
| `customer.corporateAddress.state` | string | no |  |
| `customer.corporateAddress.zip` | string | no |  |
| `customer.corporateContact` | object | no |  |
| `customer.corporateContact.firstName` | string | no |  |
| `customer.corporateContact.lastName` | string | no |  |
| `customer.corporateContact.email` | string | no |  |
| `customer.corporateContact.phone` | string | no |  |
| `customer.corporateContact.cellphone` | string | no |  |
| `customer.corporateContact.fax` | string | no |  |
| `customer.billingAddress` | object | no |  |
| `customer.billingAddress.line1` | string | no |  |
| `customer.billingAddress.line2` | string | no |  |
| `customer.billingAddress.city` | string | no |  |
| `customer.billingAddress.state` | string | no |  |
| `customer.billingAddress.zip` | string | no |  |
| `customer.billingContact` | object | no |  |
| `customer.billingContact.firstName` | string | no |  |
| `customer.billingContact.lastName` | string | no |  |
| `customer.billingContact.email` | string | no |  |
| `customer.billingContact.phone` | string | no |  |
| `customer.billingContact.cellphone` | string | no |  |
| `customer.billingContact.fax` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingAddress": {
        "address1": "string",
        "address2": "string",
        "city": "string",
        "state": "string",
        "zip": "string"
      },
      "billingContact": {
        "cellphone": "string",
        "email": "ava@example.com",
        "fax": "string",
        "fullname": "Ava Chen",
        "phone": "string"
      },
      "corporateAddress": {
        "address1": "string",
        "address2": "string",
        "city": "string",
        "state": "string",
        "zip": "string"
      },
      "corporateContact": {
        "cellphone": "string",
        "email": "ava@example.com",
        "fax": "string",
        "fullname": "Ava Chen",
        "phone": "string"
      },
      "email": "ava@example.com",
      "emailConfirmationToSupervisor": true,
      "externalId": "string",
      "id": 1,
      "name": "Ava Chen",
      "notes": "string",
      "optOutAutoConfirmation": true,
      "optOutEmailConfirmation": true,
      "phone": "string",
      "poRequired": true,
      "status": "string",
      "supervisor": "string",
      "workOrderNotes": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingAddress` | object |  |
| `billingAddress.address1` | string |  |
| `billingAddress.address2` | string |  |
| `billingAddress.city` | string |  |
| `billingAddress.state` | string |  |
| `billingAddress.zip` | string |  |
| `billingContact` | object |  |
| `billingContact.cellphone` | string |  |
| `billingContact.email` | string |  |
| `billingContact.fax` | string |  |
| `billingContact.fullname` | string |  |
| `billingContact.phone` | string |  |
| `corporateAddress` | object |  |
| `corporateAddress.address1` | string |  |
| `corporateAddress.address2` | string |  |
| `corporateAddress.city` | string |  |
| `corporateAddress.state` | string |  |
| `corporateAddress.zip` | string |  |
| `corporateContact` | object |  |
| `corporateContact.cellphone` | string |  |
| `corporateContact.email` | string |  |
| `corporateContact.fax` | string |  |
| `corporateContact.fullname` | string |  |
| `corporateContact.phone` | string |  |
| `email` | string |  |
| `emailConfirmationToSupervisor` | boolean |  |
| `externalId` | string |  |
| `id` | number |  |
| `name` | string |  |
| `notes` | string |  |
| `optOutAutoConfirmation` | boolean |  |
| `optOutEmailConfirmation` | boolean |  |
| `phone` | string |  |
| `poRequired` | boolean |  |
| `status` | string |  |
| `supervisor` | string |  |
| `workOrderNotes` | string |  |

## Native endpoint

Through the native ECI Bolt API, this operation is `PATCH /open/v1/customers/:id` (base URL `https://app.bolttech.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

