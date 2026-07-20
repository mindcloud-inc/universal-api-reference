# Open Charge Map Universal API Examples

These examples use the MindCloud API key and Open Charge Map connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Core Reference Data



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

Example response:

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

See the full [Get Core Reference Data action reference](actions/get-core-reference-data.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openChargeMap/latest/actions/get-core-reference-data).
