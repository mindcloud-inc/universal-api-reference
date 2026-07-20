# Amazon Seller: Get Account

Retrieves seller account and marketplace details from Amazon Seller.

```
GET https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-account?${params}`, {
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
      "business": {
        "companyRegistrationNumber": "string",
        "companyTaxIdentificationNumber": "string",
        "name": "Ava Chen",
        "nonLatinName": "Ava Chen",
        "registeredBusinessAddress": {
          "addressLine1": "string",
          "addressLine2": "string",
          "city": "string",
          "countryCode": "string",
          "postalCode": "string",
          "stateOrProvinceCode": "string"
        }
      },
      "businessType": "string",
      "marketplaceParticipationList": [
        {
          "marketplace": {
            "countryCode": "string",
            "defaultCurrencyCode": "string",
            "defaultLanguageCode": "string",
            "domainName": "Ava Chen",
            "id": "string",
            "name": "Ava Chen"
          },
          "participation": {
            "hasSuspendedListings": true,
            "isParticipating": true
          },
          "storeName": "Ava Chen"
        }
      ],
      "primaryContact": {
        "address": {
          "addressLine1": "string",
          "addressLine2": "string",
          "city": "string",
          "countryCode": "string",
          "postalCode": "string",
          "stateOrProvinceCode": "string"
        },
        "name": "Ava Chen",
        "nonLatinName": "Ava Chen"
      },
      "sellingPlan": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `business.companyRegistrationNumber` | string |  |
| `business.companyTaxIdentificationNumber` | string |  |
| `business.name` | string |  |
| `business.nonLatinName` | string |  |
| `business.registeredBusinessAddress.addressLine1` | string |  |
| `business.registeredBusinessAddress.addressLine2` | string |  |
| `business.registeredBusinessAddress.city` | string |  |
| `business.registeredBusinessAddress.countryCode` | string |  |
| `business.registeredBusinessAddress.postalCode` | string |  |
| `business.registeredBusinessAddress.stateOrProvinceCode` | string |  |
| `businessType` | string |  |
| `marketplaceParticipationList[].marketplace.countryCode` | string |  |
| `marketplaceParticipationList[].marketplace.defaultCurrencyCode` | string |  |
| `marketplaceParticipationList[].marketplace.defaultLanguageCode` | string |  |
| `marketplaceParticipationList[].marketplace.domainName` | string |  |
| `marketplaceParticipationList[].marketplace.id` | string |  |
| `marketplaceParticipationList[].marketplace.name` | string |  |
| `marketplaceParticipationList[].participation.hasSuspendedListings` | boolean |  |
| `marketplaceParticipationList[].participation.isParticipating` | boolean |  |
| `marketplaceParticipationList[].storeName` | string |  |
| `primaryContact.address.addressLine1` | string |  |
| `primaryContact.address.addressLine2` | string |  |
| `primaryContact.address.city` | string |  |
| `primaryContact.address.countryCode` | string |  |
| `primaryContact.address.postalCode` | string |  |
| `primaryContact.address.stateOrProvinceCode` | string |  |
| `primaryContact.name` | string |  |
| `primaryContact.nonLatinName` | string |  |
| `sellingPlan` | string |  |

## Native endpoint

Through the native Amazon Seller API, this operation is `GET sellers/v1/account` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

