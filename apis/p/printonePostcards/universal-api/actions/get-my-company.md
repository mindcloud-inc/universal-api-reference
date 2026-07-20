# Print.one Postcards: Get My Company

Retrieves your company details from Print.one Postcards.

```
GET https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/get-my-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Print.one Postcards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/get-my-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/get-my-company?${params}`, {
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
      "canBeBilled": true,
      "city": "string",
      "cocNumber": "string",
      "companyName": "Ava Chen",
      "country": "string",
      "createdAt": "string",
      "email": "ava@example.com",
      "emailVerifiedAt": "ava@example.com",
      "financialContactEmail": "ava@example.com",
      "financialContactName": "Ava Chen",
      "firstName": "Ava",
      "forceTwoFactor": true,
      "houseNumber": "string",
      "iban": "string",
      "id": "string",
      "invoiceEmail": "ava@example.com",
      "invoicingPolicy": "string",
      "lastLoginAt": "string",
      "lastName": "Chen",
      "phoneNumber": "string",
      "phonePrefix": "string",
      "planId": "string",
      "postalCode": "string",
      "postpaidLimit": 1,
      "region": "string",
      "returnAddressee": "string",
      "returnCity": "string",
      "returnCountry": "string",
      "returnHouseNumber": "string",
      "returnPostalCode": "string",
      "returnStreet": "string",
      "secondAddressLine": "string",
      "street": "string",
      "technicalContactEmail": "ava@example.com",
      "technicalContactName": "Ava Chen",
      "updatedAt": "string",
      "vatNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canBeBilled` | boolean |  |
| `city` | string |  |
| `cocNumber` | string |  |
| `companyName` | string |  |
| `country` | string |  |
| `createdAt` | string |  |
| `email` | string |  |
| `emailVerifiedAt` | string |  |
| `financialContactEmail` | string |  |
| `financialContactName` | string |  |
| `firstName` | string |  |
| `forceTwoFactor` | boolean |  |
| `houseNumber` | string |  |
| `iban` | string |  |
| `id` | string |  |
| `invoiceEmail` | string |  |
| `invoicingPolicy` | string |  |
| `lastLoginAt` | string |  |
| `lastName` | string |  |
| `phoneNumber` | string |  |
| `phonePrefix` | string |  |
| `planId` | string |  |
| `postalCode` | string |  |
| `postpaidLimit` | number |  |
| `region` | string |  |
| `returnAddressee` | string |  |
| `returnCity` | string |  |
| `returnCountry` | string |  |
| `returnHouseNumber` | string |  |
| `returnPostalCode` | string |  |
| `returnStreet` | string |  |
| `secondAddressLine` | string |  |
| `street` | string |  |
| `technicalContactEmail` | string |  |
| `technicalContactName` | string |  |
| `updatedAt` | string |  |
| `vatNumber` | string |  |

## Native endpoint

Through the native Print.one Postcards API, this operation is `GET /v2/companies/me` (base URL `https://api.print.one`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-company.md) for the provider-specific parameters and requirements.

