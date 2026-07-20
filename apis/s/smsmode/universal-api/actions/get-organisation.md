# smsmode: Get Organisation



```
GET https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/get-organisation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smsmode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/get-organisation?connectionId=$CONNECTION_ID&organisationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organisationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/get-organisation?${params}`, {
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
| `organisationId` | string | yes | Organisation ID path parameter from the smsmode API route. |

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
        "amount": 1,
        "currency": "string",
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
      "creationDate": "2026-05-07T12:00:00.000Z",
      "href": "string",
      "monthlyConsumption": 1,
      "monthlyConsumptionLimit": 1,
      "name": "Ava Chen",
      "organisationId": "string",
      "parentOrganisationId": "string",
      "state": "string"
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
| `balance.amount` | number |  |
| `balance.currency` | string |  |
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
| `creationDate` | date |  |
| `href` | string |  |
| `monthlyConsumption` | number |  |
| `monthlyConsumptionLimit` | number |  |
| `name` | string |  |
| `organisationId` | string |  |
| `parentOrganisationId` | string |  |
| `state` | string |  |

## Native endpoint

Through the native smsmode API, this operation is `GET commons/v1/organisations/:organisationId` (base URL `https://rest.smsmode.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organisation.md) for the provider-specific parameters and requirements.

