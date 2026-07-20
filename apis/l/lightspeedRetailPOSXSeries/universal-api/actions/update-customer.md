# Lightspeed Retail POS (X-Series): Update Customer

Updates an existing customer in Lightspeed Retail POS (X-Series).

```
PUT https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightspeed Retail POS (X-Series) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "string",
  "firstName": "Ava",
  "lastName": "Chen",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "string",
    "firstName": "Ava",
    "lastName": "Chen",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | yes | The customer ID to update |
| `firstName` | string | yes | Updated first name |
| `lastName` | string | yes | Updated last name |
| `email` | string | yes | Updated email address |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": "string",
      "companyName": "Ava Chen",
      "contactSource": "string",
      "createdAt": "string",
      "customerCode": "string",
      "customerGroupId": "string",
      "customerGroupIds": "string",
      "customField1": "string",
      "customField2": "string",
      "customField3": "string",
      "customField4": "string",
      "dateOfBirth": "string",
      "deletedAt": "string",
      "doNotEmail": "ava@example.com",
      "email": "ava@example.com",
      "enableLoyalty": "string",
      "enablePromotionalSms": "string",
      "fax": "string",
      "firstName": "Ava",
      "gender": "string",
      "id": "string",
      "lastName": "Chen",
      "loyaltyBalance": "string",
      "mobile": "string",
      "name": "Ava Chen",
      "note": "string",
      "onAccountLimit": "string",
      "phone": "string",
      "physicalAddress1": "string",
      "physicalAddress2": "string",
      "physicalCity": "string",
      "physicalCountryId": "string",
      "physicalPostcode": "string",
      "physicalState": "string",
      "physicalSuburb": "string",
      "postalAddress1": "string",
      "postalAddress2": "string",
      "postalCity": "string",
      "postalCountryId": "string",
      "postalPostcode": "string",
      "postalState": "string",
      "postalSuburb": "string",
      "taxId": "string",
      "twitter": "string",
      "updatedAt": "string",
      "version": "string",
      "website": "string",
      "yearToDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | string |  |
| `companyName` | string |  |
| `contactSource` | string |  |
| `createdAt` | string |  |
| `customerCode` | string |  |
| `customerGroupId` | string |  |
| `customerGroupIds` | string |  |
| `customField1` | string |  |
| `customField2` | string |  |
| `customField3` | string |  |
| `customField4` | string |  |
| `dateOfBirth` | string |  |
| `deletedAt` | string |  |
| `doNotEmail` | string |  |
| `email` | string |  |
| `enableLoyalty` | string |  |
| `enablePromotionalSms` | string |  |
| `fax` | string |  |
| `firstName` | string |  |
| `gender` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `loyaltyBalance` | string |  |
| `mobile` | string |  |
| `name` | string |  |
| `note` | string |  |
| `onAccountLimit` | string |  |
| `phone` | string |  |
| `physicalAddress1` | string |  |
| `physicalAddress2` | string |  |
| `physicalCity` | string |  |
| `physicalCountryId` | string |  |
| `physicalPostcode` | string |  |
| `physicalState` | string |  |
| `physicalSuburb` | string |  |
| `postalAddress1` | string |  |
| `postalAddress2` | string |  |
| `postalCity` | string |  |
| `postalCountryId` | string |  |
| `postalPostcode` | string |  |
| `postalState` | string |  |
| `postalSuburb` | string |  |
| `taxId` | string |  |
| `twitter` | string |  |
| `updatedAt` | string |  |
| `version` | string |  |
| `website` | string |  |
| `yearToDate` | string |  |

## Native endpoint

Through the native Lightspeed Retail POS (X-Series) API, this operation is `PUT /api/2.0/customers/:customer_id` (base URL `https://{{credentials.authorizeRequest.domain_prefix}}.retail.lightspeed.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

