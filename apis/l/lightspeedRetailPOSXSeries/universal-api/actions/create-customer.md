# Lightspeed Retail POS (X-Series): Create Customer

Creates a new customer in Lightspeed Retail POS (X-Series).

```
POST https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightspeed Retail POS (X-Series) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `firstName` | string | yes | The customer's first name. |
| `lastName` | string | yes | The customer's last name. |
| `email` | string | yes | The customer's email address. |

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

Through the native Lightspeed Retail POS (X-Series) API, this operation is `POST /api/2.0/customers` (base URL `https://{{credentials.authorizeRequest.domain_prefix}}.retail.lightspeed.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

