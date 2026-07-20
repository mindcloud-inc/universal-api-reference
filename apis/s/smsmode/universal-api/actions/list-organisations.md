# smsmode: List Organisations



```
GET https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/list-organisations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smsmode `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/list-organisations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/list-organisations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native smsmode API, this operation is `GET commons/v1/organisations` (base URL `https://rest.smsmode.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-organisations.md) for the provider-specific parameters and requirements.

