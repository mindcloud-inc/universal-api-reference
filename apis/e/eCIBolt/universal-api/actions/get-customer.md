# ECI Bolt: Get Customer



```
GET https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECI Bolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/get-customer?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/get-customer?${params}`, {
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
| `id` | number | yes | Id of the customer. |

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

Through the native ECI Bolt API, this operation is `GET /open/v1/customers/:id` (base URL `https://app.bolttech.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

