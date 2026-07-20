# Open Charge Map: Get Core Reference Data



```
GET https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/get-core-reference-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Charge Map `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/get-core-reference-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/get-core-reference-data?${params}`, {
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
      "chargePoint": {
        "addressInfo": {
          "accessComments": {},
          "addressLine1": {},
          "addressLine2": {},
          "contactEmail": {},
          "contactTelephone1": {},
          "contactTelephone2": {},
          "country": {},
          "countryID": {},
          "distance": {},
          "distanceUnit": 1,
          "id": 1,
          "latitude": 1,
          "longitude": 1,
          "postcode": {},
          "relatedURL": {},
          "stateOrProvince": {},
          "title": {},
          "town": {}
        },
        "connections": [
          {
            "amps": {},
            "comments": {},
            "connectionType": {},
            "connectionTypeID": {},
            "currentType": {},
            "currentTypeID": {},
            "id": 1,
            "level": {},
            "levelID": {},
            "powerKW": {},
            "quantity": {},
            "reference": {},
            "statusType": {},
            "statusTypeID": {},
            "voltage": {}
          }
        ],
        "dataProvider": {
          "comments": {},
          "dataProviderStatusType": {},
          "dateLastImported": {},
          "id": 1,
          "isApprovedImport": {},
          "isOpenDataLicensed": {},
          "isRestrictedEdit": true,
          "license": {},
          "title": {},
          "websiteURL": {}
        },
        "dataProviderID": {},
        "dataProvidersReference": {},
        "dataQualityLevel": 1,
        "dateCreated": "string",
        "dateLastConfirmed": "string",
        "dateLastStatusUpdate": "string",
        "dateLastVerified": "string",
        "datePlanned": {},
        "generalComments": "string",
        "id": 1,
        "isRecentlyVerified": true,
        "mediaItems": {},
        "metadataValues": {},
        "numberOfPoints": 1,
        "operatorID": {},
        "operatorInfo": {
          "addressInfo": {},
          "bookingURL": {},
          "comments": {},
          "contactEmail": {},
          "faultReportEmail": {},
          "id": 1,
          "isPrivateIndividual": {},
          "isRestrictedEdit": {},
          "phonePrimaryContact": {},
          "phoneSecondaryContact": {},
          "title": {},
          "websiteURL": {}
        },
        "operatorsReference": {},
        "parentChargePointID": {},
        "percentageSimilarity": {},
        "statusType": {
          "id": 1,
          "isOperational": {},
          "isUserSelectable": true,
          "title": {}
        },
        "statusTypeID": {},
        "submissionStatus": {},
        "submissionStatusTypeID": {},
        "usageCost": {},
        "usageType": {
          "id": 1,
          "isAccessKeyRequired": {},
          "isMembershipRequired": {},
          "isPayAtLocation": {},
          "title": {}
        },
        "usageTypeID": {},
        "userComments": {},
        "uuid": "string"
      },
      "chargerTypes": [
        {
          "comments": "string",
          "id": 1,
          "isFastChargeCapable": true,
          "title": "string"
        }
      ],
      "checkinStatusTypes": [
        {
          "id": 1,
          "isAutomatedCheckin": true,
          "isPositive": {},
          "title": "string"
        }
      ],
      "connectionTypes": [
        {
          "formalName": "Ava Chen",
          "id": 1,
          "isDiscontinued": true,
          "isObsolete": true,
          "title": "string"
        }
      ],
      "countries": [
        {
          "continentCode": "string",
          "id": 1,
          "iSOCode": "string",
          "title": "string"
        }
      ],
      "currentTypes": [
        {
          "description": "string",
          "id": 1,
          "title": "string"
        }
      ],
      "dataProviders": [
        {
          "comments": {},
          "dataProviderStatusType": {
            "id": 1,
            "isProviderEnabled": true,
            "title": "string"
          },
          "dateLastImported": {},
          "id": 1,
          "isApprovedImport": true,
          "isOpenDataLicensed": true,
          "isRestrictedEdit": true,
          "license": "string",
          "title": "string",
          "websiteURL": "https://example.com"
        }
      ],
      "dataTypes": [
        {
          "id": 1,
          "title": "string"
        }
      ],
      "metadataGroups": [
        {
          "dataProviderID": 1,
          "id": 1,
          "isPublicInterest": true,
          "isRestrictedEdit": true,
          "metadataFields": [
            {
              "dataType": {},
              "dataTypeID": 1,
              "id": 1,
              "metadataFieldOptions": [
                {
                  "id": 1,
                  "metadataFieldID": 1,
                  "title": "string"
                }
              ],
              "metadataGroupID": 1,
              "title": "string"
            }
          ],
          "title": "string"
        }
      ],
      "operators": [
        {
          "addressInfo": {},
          "bookingURL": {},
          "comments": "string",
          "contactEmail": {},
          "faultReportEmail": {},
          "id": 1,
          "isPrivateIndividual": true,
          "isRestrictedEdit": {},
          "phonePrimaryContact": {},
          "phoneSecondaryContact": {},
          "title": "string",
          "websiteURL": {}
        }
      ],
      "statusTypes": [
        {
          "id": 1,
          "isOperational": {},
          "isUserSelectable": true,
          "title": "string"
        }
      ],
      "submissionStatusTypes": [
        {
          "id": 1,
          "isLive": true,
          "title": "string"
        }
      ],
      "usageTypes": [
        {
          "id": 1,
          "isAccessKeyRequired": {},
          "isMembershipRequired": {},
          "isPayAtLocation": {},
          "title": "string"
        }
      ],
      "userComment": {
        "chargePointID": 1,
        "checkinStatusType": {
          "id": 1,
          "isAutomatedCheckin": true,
          "isPositive": {},
          "title": "string"
        },
        "checkinStatusTypeID": {},
        "comment": "string",
        "commentType": {
          "id": 1,
          "title": "string"
        },
        "commentTypeID": {},
        "dateCreated": "string",
        "id": 1,
        "isActionedByEditor": {},
        "rating": {},
        "relatedURL": {},
        "user": {},
        "userName": {}
      },
      "userCommentTypes": [
        {
          "id": 1,
          "title": "string"
        }
      ],
      "userProfile": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chargePoint.addressInfo.accessComments` | object |  |
| `chargePoint.addressInfo.addressLine1` | object |  |
| `chargePoint.addressInfo.addressLine2` | object |  |
| `chargePoint.addressInfo.contactEmail` | object |  |
| `chargePoint.addressInfo.contactTelephone1` | object |  |
| `chargePoint.addressInfo.contactTelephone2` | object |  |
| `chargePoint.addressInfo.country` | object |  |
| `chargePoint.addressInfo.countryID` | object |  |
| `chargePoint.addressInfo.distance` | object |  |
| `chargePoint.addressInfo.distanceUnit` | number |  |
| `chargePoint.addressInfo.id` | number |  |
| `chargePoint.addressInfo.latitude` | number |  |
| `chargePoint.addressInfo.longitude` | number |  |
| `chargePoint.addressInfo.postcode` | object |  |
| `chargePoint.addressInfo.relatedURL` | object |  |
| `chargePoint.addressInfo.stateOrProvince` | object |  |
| `chargePoint.addressInfo.title` | object |  |
| `chargePoint.addressInfo.town` | object |  |
| `chargePoint.connections[].amps` | object |  |
| `chargePoint.connections[].comments` | object |  |
| `chargePoint.connections[].connectionType` | object |  |
| `chargePoint.connections[].connectionTypeID` | object |  |
| `chargePoint.connections[].currentType` | object |  |
| `chargePoint.connections[].currentTypeID` | object |  |
| `chargePoint.connections[].id` | number |  |
| `chargePoint.connections[].level` | object |  |
| `chargePoint.connections[].levelID` | object |  |
| `chargePoint.connections[].powerKW` | object |  |
| `chargePoint.connections[].quantity` | object |  |
| `chargePoint.connections[].reference` | object |  |
| `chargePoint.connections[].statusType` | object |  |
| `chargePoint.connections[].statusTypeID` | object |  |
| `chargePoint.connections[].voltage` | object |  |
| `chargePoint.dataProvider.comments` | object |  |
| `chargePoint.dataProvider.dataProviderStatusType` | object |  |
| `chargePoint.dataProvider.dateLastImported` | object |  |
| `chargePoint.dataProvider.id` | number |  |
| `chargePoint.dataProvider.isApprovedImport` | object |  |
| `chargePoint.dataProvider.isOpenDataLicensed` | object |  |
| `chargePoint.dataProvider.isRestrictedEdit` | boolean |  |
| `chargePoint.dataProvider.license` | object |  |
| `chargePoint.dataProvider.title` | object |  |
| `chargePoint.dataProvider.websiteURL` | object |  |
| `chargePoint.dataProviderID` | object |  |
| `chargePoint.dataProvidersReference` | object |  |
| `chargePoint.dataQualityLevel` | number |  |
| `chargePoint.dateCreated` | string |  |
| `chargePoint.dateLastConfirmed` | string |  |
| `chargePoint.dateLastStatusUpdate` | string |  |
| `chargePoint.dateLastVerified` | string |  |
| `chargePoint.datePlanned` | object |  |
| `chargePoint.generalComments` | string |  |
| `chargePoint.id` | number |  |
| `chargePoint.isRecentlyVerified` | boolean |  |
| `chargePoint.mediaItems` | object |  |
| `chargePoint.metadataValues` | object |  |
| `chargePoint.numberOfPoints` | number |  |
| `chargePoint.operatorID` | object |  |
| `chargePoint.operatorInfo.addressInfo` | object |  |
| `chargePoint.operatorInfo.bookingURL` | object |  |
| `chargePoint.operatorInfo.comments` | object |  |
| `chargePoint.operatorInfo.contactEmail` | object |  |
| `chargePoint.operatorInfo.faultReportEmail` | object |  |
| `chargePoint.operatorInfo.id` | number |  |
| `chargePoint.operatorInfo.isPrivateIndividual` | object |  |
| `chargePoint.operatorInfo.isRestrictedEdit` | object |  |
| `chargePoint.operatorInfo.phonePrimaryContact` | object |  |
| `chargePoint.operatorInfo.phoneSecondaryContact` | object |  |
| `chargePoint.operatorInfo.title` | object |  |
| `chargePoint.operatorInfo.websiteURL` | object |  |
| `chargePoint.operatorsReference` | object |  |
| `chargePoint.parentChargePointID` | object |  |
| `chargePoint.percentageSimilarity` | object |  |
| `chargePoint.statusType.id` | number |  |
| `chargePoint.statusType.isOperational` | object |  |
| `chargePoint.statusType.isUserSelectable` | boolean |  |
| `chargePoint.statusType.title` | object |  |
| `chargePoint.statusTypeID` | object |  |
| `chargePoint.submissionStatus` | object |  |
| `chargePoint.submissionStatusTypeID` | object |  |
| `chargePoint.usageCost` | object |  |
| `chargePoint.usageType.id` | number |  |
| `chargePoint.usageType.isAccessKeyRequired` | object |  |
| `chargePoint.usageType.isMembershipRequired` | object |  |
| `chargePoint.usageType.isPayAtLocation` | object |  |
| `chargePoint.usageType.title` | object |  |
| `chargePoint.usageTypeID` | object |  |
| `chargePoint.userComments` | object |  |
| `chargePoint.uuid` | string |  |
| `chargerTypes[].comments` | string |  |
| `chargerTypes[].id` | number |  |
| `chargerTypes[].isFastChargeCapable` | boolean |  |
| `chargerTypes[].title` | string |  |
| `checkinStatusTypes[].id` | number |  |
| `checkinStatusTypes[].isAutomatedCheckin` | boolean |  |
| `checkinStatusTypes[].isPositive` | object |  |
| `checkinStatusTypes[].title` | string |  |
| `connectionTypes[].formalName` | string |  |
| `connectionTypes[].id` | number |  |
| `connectionTypes[].isDiscontinued` | boolean |  |
| `connectionTypes[].isObsolete` | boolean |  |
| `connectionTypes[].title` | string |  |
| `countries[].continentCode` | string |  |
| `countries[].id` | number |  |
| `countries[].iSOCode` | string |  |
| `countries[].title` | string |  |
| `currentTypes[].description` | string |  |
| `currentTypes[].id` | number |  |
| `currentTypes[].title` | string |  |
| `dataProviders[].comments` | object |  |
| `dataProviders[].dataProviderStatusType.id` | number |  |
| `dataProviders[].dataProviderStatusType.isProviderEnabled` | boolean |  |
| `dataProviders[].dataProviderStatusType.title` | string |  |
| `dataProviders[].dateLastImported` | object |  |
| `dataProviders[].id` | number |  |
| `dataProviders[].isApprovedImport` | boolean |  |
| `dataProviders[].isOpenDataLicensed` | boolean |  |
| `dataProviders[].isRestrictedEdit` | boolean |  |
| `dataProviders[].license` | string |  |
| `dataProviders[].title` | string |  |
| `dataProviders[].websiteURL` | string |  |
| `dataTypes[].id` | number |  |
| `dataTypes[].title` | string |  |
| `metadataGroups[].dataProviderID` | number |  |
| `metadataGroups[].id` | number |  |
| `metadataGroups[].isPublicInterest` | boolean |  |
| `metadataGroups[].isRestrictedEdit` | boolean |  |
| `metadataGroups[].metadataFields[].dataType` | object |  |
| `metadataGroups[].metadataFields[].dataTypeID` | number |  |
| `metadataGroups[].metadataFields[].id` | number |  |
| `metadataGroups[].metadataFields[].metadataFieldOptions[].id` | number |  |
| `metadataGroups[].metadataFields[].metadataFieldOptions[].metadataFieldID` | number |  |
| `metadataGroups[].metadataFields[].metadataFieldOptions[].title` | string |  |
| `metadataGroups[].metadataFields[].metadataGroupID` | number |  |
| `metadataGroups[].metadataFields[].title` | string |  |
| `metadataGroups[].title` | string |  |
| `operators[].addressInfo` | object |  |
| `operators[].bookingURL` | object |  |
| `operators[].comments` | string |  |
| `operators[].contactEmail` | object |  |
| `operators[].faultReportEmail` | object |  |
| `operators[].id` | number |  |
| `operators[].isPrivateIndividual` | boolean |  |
| `operators[].isRestrictedEdit` | object |  |
| `operators[].phonePrimaryContact` | object |  |
| `operators[].phoneSecondaryContact` | object |  |
| `operators[].title` | string |  |
| `operators[].websiteURL` | object |  |
| `statusTypes[].id` | number |  |
| `statusTypes[].isOperational` | object |  |
| `statusTypes[].isUserSelectable` | boolean |  |
| `statusTypes[].title` | string |  |
| `submissionStatusTypes[].id` | number |  |
| `submissionStatusTypes[].isLive` | boolean |  |
| `submissionStatusTypes[].title` | string |  |
| `usageTypes[].id` | number |  |
| `usageTypes[].isAccessKeyRequired` | object |  |
| `usageTypes[].isMembershipRequired` | object |  |
| `usageTypes[].isPayAtLocation` | object |  |
| `usageTypes[].title` | string |  |
| `userComment.chargePointID` | number |  |
| `userComment.checkinStatusType.id` | number |  |
| `userComment.checkinStatusType.isAutomatedCheckin` | boolean |  |
| `userComment.checkinStatusType.isPositive` | object |  |
| `userComment.checkinStatusType.title` | string |  |
| `userComment.checkinStatusTypeID` | object |  |
| `userComment.comment` | string |  |
| `userComment.commentType.id` | number |  |
| `userComment.commentType.title` | string |  |
| `userComment.commentTypeID` | object |  |
| `userComment.dateCreated` | string |  |
| `userComment.id` | number |  |
| `userComment.isActionedByEditor` | object |  |
| `userComment.rating` | object |  |
| `userComment.relatedURL` | object |  |
| `userComment.user` | object |  |
| `userComment.userName` | object |  |
| `userCommentTypes[].id` | number |  |
| `userCommentTypes[].title` | string |  |
| `userProfile` | object |  |

## Native endpoint

Through the native Open Charge Map API, this operation is `GET /referencedata` (base URL `https://api.openchargemap.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-core-reference-data.md) for the provider-specific parameters and requirements.

