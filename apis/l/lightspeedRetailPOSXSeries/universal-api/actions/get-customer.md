# Lightspeed Retail POS (X-Series): Get Customer

Retrieves a customer from Lightspeed Retail POS (X-Series).

```
GET https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightspeed Retail POS (X-Series) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/get-customer?connectionId=$CONNECTION_ID&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/get-customer?${params}`, {
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
| `customerId` | string | yes | The Lightspeed customer ID to retrieve. |

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
      "loyaltyEmailSent": "ava@example.com",
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
      "sourceUniqueId": "string",
      "taxId": "string",
      "timeUntilDeletion": "string",
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
| `loyaltyEmailSent` | string |  |
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
| `sourceUniqueId` | string |  |
| `taxId` | string |  |
| `timeUntilDeletion` | string |  |
| `twitter` | string |  |
| `updatedAt` | string |  |
| `version` | string |  |
| `website` | string |  |
| `yearToDate` | string |  |

## Native endpoint

Through the native Lightspeed Retail POS (X-Series) API, this operation is `GET /api/2.0/customers/:customer_id` (base URL `https://{{credentials.authorizeRequest.domain_prefix}}.retail.lightspeed.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

