# Centerpoint: Update Company



```
PUT https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/update-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/update-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "COMPANY_ID": "593838"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/update-company', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "COMPANY_ID": "593838"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `COMPANY_ID` | string | yes | Example: `593838`. |
| `name` | string | no |  |
| `type` | list<string> | no | One of: `Admin`, `Company`, `Contractor`, `Corporate`, `Residential`, `Vendor`. |
| `salesStatus` | list<string> | no | One of: `Dead`, `Lead`, `Quoted`, `Sold`. |
| `timeZone` | list<string> | no | One of: `America/Anchorage`, `America/Chicago`, `America/Denver`, `America/Detroit`, `America/Los_Angeles`, `America/New_York`, `America/Phoenix`, `Pacific/Honolulu`. |
| `custom.customerType` | string | no |  |
| `options.taxLabelOverride` | string | no |  |
| `custom.companyPhoneNumber` | string | no |  |
| `options.billingAddress` | string | no |  |
| `options.isCreditHold` | boolean | no |  |
| `options.isTaxExempt` | boolean | no |  |
| `options.serviceBillingInstructions` | string | no |  |
| `isBilling` | boolean | no |  |
| `isActive` | boolean | no |  |
| `options.serviceWorkInstructions` | string | no |  |
| `options.laborRates` | string | no |  |
| `email` | string | no |  |
| `streetAddress` | string | no |  |
| `subpremise` | string | no |  |
| `locality` | string | no |  |
| `county` | string | no |  |
| `region` | string | no |  |
| `postalCode` | string | no |  |
| `country` | string | no |  |
| `latitude` | number | no |  |
| `longitude` | number | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `placeID` | string | no |  |
| `externalID` | string | no |  |
| `importID` | string | no |  |
| `managerID` | string | no |  |
| `website` | string | no |  |
| `imageID` | string | no |  |
| `closeRate` | number | no |  |
| `options` | object | no |  |
| `custom` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "accountId": 1,
        "closeRate": "string",
        "country": "string",
        "county": "string",
        "createdAt": "string",
        "custom": {
          "licensed": {}
        },
        "customWithLabels": {
          "licensed": {}
        },
        "deletedAt": {},
        "externalId": "string",
        "importId": {},
        "latitude": 1,
        "locality": "string",
        "longitude": 1,
        "name": "Ava Chen",
        "options": {
          "dailyProgressReportIncludedWork": "string",
          "dailyProgressReportTimeOfDay": "string",
          "isHideProductPriceFromTechnicians": true,
          "serviceBillingInstructions": "string",
          "taxLabelOverride": "string"
        },
        "placeId": "string",
        "postalCode": "string",
        "propertyCount": 1,
        "recentActivity": "string",
        "region": "string",
        "salesStatus": "string",
        "streetAddress": "string",
        "subpremise": {},
        "timezone": "string",
        "type": "string",
        "updatedAt": "string",
        "website": {}
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.accountId` | number |  |
| `attributes.closeRate` | string |  |
| `attributes.country` | string |  |
| `attributes.county` | string |  |
| `attributes.createdAt` | string |  |
| `attributes.custom.licensed` | object |  |
| `attributes.customWithLabels.licensed` | object |  |
| `attributes.deletedAt` | object |  |
| `attributes.externalId` | string |  |
| `attributes.importId` | object |  |
| `attributes.latitude` | number |  |
| `attributes.locality` | string |  |
| `attributes.longitude` | number |  |
| `attributes.name` | string |  |
| `attributes.options.dailyProgressReportIncludedWork` | string |  |
| `attributes.options.dailyProgressReportTimeOfDay` | string |  |
| `attributes.options.isHideProductPriceFromTechnicians` | boolean |  |
| `attributes.options.serviceBillingInstructions` | string |  |
| `attributes.options.taxLabelOverride` | string |  |
| `attributes.placeId` | string |  |
| `attributes.postalCode` | string |  |
| `attributes.propertyCount` | number |  |
| `attributes.recentActivity` | string |  |
| `attributes.region` | string |  |
| `attributes.salesStatus` | string |  |
| `attributes.streetAddress` | string |  |
| `attributes.subpremise` | object |  |
| `attributes.timezone` | string |  |
| `attributes.type` | string |  |
| `attributes.updatedAt` | string |  |
| `attributes.website` | object |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `PATCH companies/:COMPANY_ID` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-company.md) for the provider-specific parameters and requirements.

