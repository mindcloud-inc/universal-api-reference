# Aspire: List Properties

List physical locations where work is performed. Click Property for more information.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-properties?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-properties?${params}`, {
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
| `expand` | string | no |  |
| `filter` | string | no |  |
| `orderBy` | string | no |  |
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountOwnerContactID": {},
      "accountOwnerContactName": {},
      "active": true,
      "activeOpportunityID": {},
      "branchCode": "string",
      "branchID": 1,
      "branchName": "Ava Chen",
      "budget": {},
      "collectionNotes": {},
      "competitorID": {},
      "countyID": {},
      "createdByUserID": 1,
      "createdByUserName": "Ava Chen",
      "createdDate": "string",
      "dragDropGeoLocation": {},
      "earliestOpportunityWonDate": {},
      "emailInvoice": true,
      "gEOLocationLatitude": {},
      "gEOLocationLongitude": {},
      "gEOPerimeter": {},
      "gPSGeofenceID": {},
      "gPSUpdated": true,
      "industryID": {},
      "industryName": {},
      "integrationID": {},
      "leadSourceID": {},
      "leadSourceName": {},
      "localityID": {},
      "localityName": {},
      "modifiedByUserID": 1,
      "modifiedByUserName": "Ava Chen",
      "modifiedDate": "string",
      "note": {},
      "paymentTermsID": {},
      "paymentTermsName": {},
      "productionManagerContactID": {},
      "productionManagerContactName": {},
      "productionNote": {},
      "propertyAddressCity": {},
      "propertyAddressID": 1,
      "propertyAddressLine1": {},
      "propertyAddressLine2": {},
      "propertyAddressStateProvinceCode": {},
      "propertyAddressZipCode": {},
      "propertyGroupID": {},
      "propertyGroupName": {},
      "propertyID": 1,
      "propertyName": {},
      "propertyNameAbr": {},
      "propertyStatusID": {},
      "propertyStatusName": {},
      "propertyType": {},
      "propertyTypeID": {},
      "propertyTypeIntegrationCode": {},
      "separateInvoices": {},
      "sequenceNumber": {},
      "snowNote": {},
      "taxJurisdictionID": {},
      "taxJurisdictionName": {},
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountOwnerContactID` | object |  |
| `accountOwnerContactName` | object |  |
| `active` | boolean |  |
| `activeOpportunityID` | object |  |
| `branchCode` | string |  |
| `branchID` | number |  |
| `branchName` | string |  |
| `budget` | object |  |
| `collectionNotes` | object |  |
| `competitorID` | object |  |
| `countyID` | object |  |
| `createdByUserID` | number |  |
| `createdByUserName` | string |  |
| `createdDate` | string |  |
| `dragDropGeoLocation` | object |  |
| `earliestOpportunityWonDate` | object |  |
| `emailInvoice` | boolean |  |
| `gEOLocationLatitude` | object |  |
| `gEOLocationLongitude` | object |  |
| `gEOPerimeter` | object |  |
| `gPSGeofenceID` | object |  |
| `gPSUpdated` | boolean |  |
| `industryID` | object |  |
| `industryName` | object |  |
| `integrationID` | object |  |
| `leadSourceID` | object |  |
| `leadSourceName` | object |  |
| `localityID` | object |  |
| `localityName` | object |  |
| `modifiedByUserID` | number |  |
| `modifiedByUserName` | string |  |
| `modifiedDate` | string |  |
| `note` | object |  |
| `paymentTermsID` | object |  |
| `paymentTermsName` | object |  |
| `productionManagerContactID` | object |  |
| `productionManagerContactName` | object |  |
| `productionNote` | object |  |
| `propertyAddressCity` | object |  |
| `propertyAddressID` | number |  |
| `propertyAddressLine1` | object |  |
| `propertyAddressLine2` | object |  |
| `propertyAddressStateProvinceCode` | object |  |
| `propertyAddressZipCode` | object |  |
| `propertyGroupID` | object |  |
| `propertyGroupName` | object |  |
| `propertyID` | number |  |
| `propertyName` | object |  |
| `propertyNameAbr` | object |  |
| `propertyStatusID` | object |  |
| `propertyStatusName` | object |  |
| `propertyType` | object |  |
| `propertyTypeID` | object |  |
| `propertyTypeIntegrationCode` | object |  |
| `separateInvoices` | object |  |
| `sequenceNumber` | object |  |
| `snowNote` | object |  |
| `taxJurisdictionID` | object |  |
| `taxJurisdictionName` | object |  |
| `website` | string |  |

## Native endpoint

Through the native Aspire API, this operation is `GET Properties` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-properties.md) for the provider-specific parameters and requirements.

