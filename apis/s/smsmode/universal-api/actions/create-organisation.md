# smsmode: Create Organisation



```
POST https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/create-organisation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smsmode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/create-organisation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "contact": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/create-organisation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "contact": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name request body field documented by the smsmode API. |
| `contact` | object | yes | Contact request body field documented by the smsmode API. |
| `address` | object | no | Address request body field documented by the smsmode API. |
| `billingContact` | object | no | Billing Contact request body field documented by the smsmode API. |
| `billingAddress` | object | no | Billing Address request body field documented by the smsmode API. |
| `companyInformation` | object | no | Company Information request body field documented by the smsmode API. |
| `balance` | object | no | Balance request body field documented by the smsmode API. |
| `monthlyConsumptionLimit` | number | no | Monthly Consumption Limit request body field documented by the smsmode API. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "address1": "string",
        "address2": "string",
        "city": "string",
        "country": "string",
        "zipCode": "string"
      },
      "balance": {
        "parentBilling": true,
        "paymentType": "string"
      },
      "billingAddress": {
        "address1": "string",
        "address2": "string",
        "city": "string",
        "country": "string",
        "zipCode": "string"
      },
      "billingContact": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "mobile": "string"
      },
      "companyInformation": {
        "name": "Ava Chen",
        "registrationNumber": "string",
        "vatNumber": "string",
        "website": "string"
      },
      "contact": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "mobile": "string"
      },
      "monthlyConsumptionLimit": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.address1` | string |  |
| `address.address2` | string |  |
| `address.city` | string |  |
| `address.country` | string |  |
| `address.zipCode` | string |  |
| `balance.parentBilling` | boolean |  |
| `balance.paymentType` | string |  |
| `billingAddress.address1` | string |  |
| `billingAddress.address2` | string |  |
| `billingAddress.city` | string |  |
| `billingAddress.country` | string |  |
| `billingAddress.zipCode` | string |  |
| `billingContact.email` | string |  |
| `billingContact.firstName` | string |  |
| `billingContact.lastName` | string |  |
| `billingContact.mobile` | string |  |
| `companyInformation.name` | string |  |
| `companyInformation.registrationNumber` | string |  |
| `companyInformation.vatNumber` | string |  |
| `companyInformation.website` | string |  |
| `contact.email` | string |  |
| `contact.firstName` | string |  |
| `contact.lastName` | string |  |
| `contact.mobile` | string |  |
| `monthlyConsumptionLimit` | number |  |
| `name` | string |  |

## Native endpoint

Through the native smsmode API, this operation is `POST commons/v1/organisations` (base URL `https://rest.smsmode.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-organisation.md) for the provider-specific parameters and requirements.

