# ADP: List Workers

Request the list of all available workers.

```
GET https://connect.mindcloud.co/v1/universal/adp/latest/actions/get-workers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ADP `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adp/latest/actions/get-workers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adp/latest/actions/get-workers?${params}`, {
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
| `filter` | string | no | **Example:** - workers/workAssignments/positionID eq 'MR2000056' |
| `changedSince` | string | no |  |
| `expand` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "associateOID": "string",
      "Base": "string",
      "customFieldGroup": {
        "codeFields": [
          {
            "itemID": "string",
            "nameCode": {
              "codeValue": "Ava Chen",
              "shortName": "Ava Chen"
            }
          }
        ],
        "dateFields": [
          {
            "itemID": "string",
            "nameCode": {
              "codeValue": "Ava Chen",
              "longName": "Ava Chen"
            }
          }
        ],
        "indicatorFields": [
          {
            "itemID": "string",
            "nameCode": {
              "codeValue": "Ava Chen",
              "longName": "Ava Chen"
            }
          }
        ],
        "numberFields": [
          {
            "itemID": "string",
            "nameCode": {
              "codeValue": "Ava Chen",
              "shortName": "Ava Chen"
            },
            "numberValue": 1
          }
        ],
        "percentFields": [
          {
            "itemID": "string",
            "nameCode": {
              "codeValue": "Ava Chen",
              "shortName": "Ava Chen"
            }
          }
        ],
        "stringFields": [
          {
            "itemID": "string",
            "nameCode": {
              "codeValue": "Ava Chen",
              "longName": "Ava Chen"
            },
            "stringValue": "string"
          }
        ]
      },
      "person": {
        "birthDate": "string",
        "communication": {
          "landlines": [
            {
              "access": "string",
              "areaDialing": "string",
              "countryDialing": "string",
              "dialNumber": "string",
              "formattedNumber": "string",
              "itemID": "string",
              "nameCode": {
                "codeValue": "Ava Chen",
                "shortName": "Ava Chen"
              }
            }
          ]
        },
        "disabledIndicator": true,
        "ethnicityCode": {
          "codeValue": "string",
          "longName": "Ava Chen",
          "shortName": "Ava Chen"
        },
        "genderCode": {
          "codeValue": "string",
          "longName": "Ava Chen",
          "shortName": "Ava Chen"
        },
        "governmentIDs": [
          {
            "countryCode": "string",
            "idValue": "string",
            "itemID": "string",
            "nameCode": {
              "codeValue": "Ava Chen",
              "longName": "Ava Chen"
            }
          }
        ],
        "legalAddress": {
          "cityName": "Ava Chen",
          "countryCode": "string",
          "countrySubdivisionLevel1": {
            "codeValue": "string",
            "shortName": "Ava Chen",
            "subdivisionType": "string"
          },
          "lineOne": "string",
          "nameCode": {
            "codeValue": "Ava Chen",
            "longName": "Ava Chen",
            "shortName": "Ava Chen"
          },
          "postalCode": "string"
        },
        "legalName": {
          "familyName1": "Ava Chen",
          "formattedName": "Ava Chen",
          "givenName": "Ava Chen"
        },
        "raceCode": {
          "codeValue": "string",
          "longName": "Ava Chen",
          "shortName": "Ava Chen"
        },
        "tobaccoUserIndicator": true
      },
      "workAssignments": [
        {
          "actualStartDate": "string",
          "assignmentStatus": {
            "effectiveDate": "string",
            "reasonCode": {
              "codeValue": "string",
              "longName": "Ava Chen"
            },
            "statusCode": {
              "codeValue": "string",
              "longName": "Ava Chen",
              "shortName": "Ava Chen"
            }
          },
          "baseRemuneration": {
            "annualRateAmount": {
              "amountValue": 1,
              "currencyCode": "string",
              "nameCode": {
                "codeValue": "Ava Chen",
                "shortName": "Ava Chen"
              }
            },
            "effectiveDate": "string",
            "hourlyRateAmount": {
              "amountValue": 1,
              "currencyCode": "https://example.com",
              "nameCode": {
                "codeValue": "https://example.com",
                "shortName": "https://example.com"
              }
            }
          },
          "hireDate": "string",
          "homeWorkLocation": {
            "address": {
              "cityName": "Ava Chen",
              "countryCode": "string",
              "countrySubdivisionLevel1": {
                "codeValue": "string",
                "shortName": "Ava Chen",
                "subdivisionType": "string"
              },
              "lineOne": "string",
              "postalCode": "string"
            },
            "nameCode": {
              "codeValue": "Ava Chen",
              "shortName": "Ava Chen"
            }
          },
          "itemID": "string",
          "managementPositionIndicator": true,
          "payCycleCode": {
            "codeValue": "string",
            "shortName": "Ava Chen"
          },
          "payrollFileNumber": "string",
          "payrollGroupCode": "string",
          "payrollProcessingStatusCode": {
            "shortName": "Ava Chen"
          },
          "payrollScheduleGroupID": "string",
          "positionID": "string",
          "primaryIndicator": true,
          "seniorityDate": "string",
          "terminationDate": "string",
          "voluntaryIndicator": true,
          "workerTimeProfile": {
            "timeAndAttendanceIndicator": true
          }
        }
      ],
      "workerDates": {
        "originalHireDate": "string",
        "terminationDate": "string"
      },
      "workerID": {
        "idValue": "string"
      },
      "workerStatus": {
        "statusCode": {
          "codeValue": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `associateOID` | string |  |
| `Base` | string |  |
| `customFieldGroup.codeFields[].itemID` | string |  |
| `customFieldGroup.codeFields[].nameCode.codeValue` | string |  |
| `customFieldGroup.codeFields[].nameCode.shortName` | string |  |
| `customFieldGroup.dateFields[].itemID` | string |  |
| `customFieldGroup.dateFields[].nameCode.codeValue` | string |  |
| `customFieldGroup.dateFields[].nameCode.longName` | string |  |
| `customFieldGroup.indicatorFields[].itemID` | string |  |
| `customFieldGroup.indicatorFields[].nameCode.codeValue` | string |  |
| `customFieldGroup.indicatorFields[].nameCode.longName` | string |  |
| `customFieldGroup.numberFields[].itemID` | string |  |
| `customFieldGroup.numberFields[].nameCode.codeValue` | string |  |
| `customFieldGroup.numberFields[].nameCode.shortName` | string |  |
| `customFieldGroup.numberFields[].numberValue` | number | Numeric custom-field value, including configured burden percentages when present. |
| `customFieldGroup.percentFields[].itemID` | string |  |
| `customFieldGroup.percentFields[].nameCode.codeValue` | string |  |
| `customFieldGroup.percentFields[].nameCode.shortName` | string |  |
| `customFieldGroup.stringFields[].itemID` | string |  |
| `customFieldGroup.stringFields[].nameCode.codeValue` | string |  |
| `customFieldGroup.stringFields[].nameCode.longName` | string |  |
| `customFieldGroup.stringFields[].stringValue` | string |  |
| `person.birthDate` | string |  |
| `person.communication.landlines[].access` | string |  |
| `person.communication.landlines[].areaDialing` | string |  |
| `person.communication.landlines[].countryDialing` | string |  |
| `person.communication.landlines[].dialNumber` | string |  |
| `person.communication.landlines[].formattedNumber` | string |  |
| `person.communication.landlines[].itemID` | string |  |
| `person.communication.landlines[].nameCode.codeValue` | string |  |
| `person.communication.landlines[].nameCode.shortName` | string |  |
| `person.disabledIndicator` | boolean |  |
| `person.ethnicityCode.codeValue` | string |  |
| `person.ethnicityCode.longName` | string |  |
| `person.ethnicityCode.shortName` | string |  |
| `person.genderCode.codeValue` | string |  |
| `person.genderCode.longName` | string |  |
| `person.genderCode.shortName` | string |  |
| `person.governmentIDs[].countryCode` | string |  |
| `person.governmentIDs[].idValue` | string |  |
| `person.governmentIDs[].itemID` | string |  |
| `person.governmentIDs[].nameCode.codeValue` | string |  |
| `person.governmentIDs[].nameCode.longName` | string |  |
| `person.legalAddress.cityName` | string |  |
| `person.legalAddress.countryCode` | string |  |
| `person.legalAddress.countrySubdivisionLevel1.codeValue` | string |  |
| `person.legalAddress.countrySubdivisionLevel1.shortName` | string |  |
| `person.legalAddress.countrySubdivisionLevel1.subdivisionType` | string |  |
| `person.legalAddress.lineOne` | string |  |
| `person.legalAddress.nameCode.codeValue` | string |  |
| `person.legalAddress.nameCode.longName` | string |  |
| `person.legalAddress.nameCode.shortName` | string |  |
| `person.legalAddress.postalCode` | string |  |
| `person.legalName.familyName1` | string |  |
| `person.legalName.formattedName` | string |  |
| `person.legalName.givenName` | string |  |
| `person.raceCode.codeValue` | string |  |
| `person.raceCode.longName` | string |  |
| `person.raceCode.shortName` | string |  |
| `person.tobaccoUserIndicator` | boolean |  |
| `workAssignments[].actualStartDate` | string |  |
| `workAssignments[].assignmentStatus.effectiveDate` | string |  |
| `workAssignments[].assignmentStatus.reasonCode.codeValue` | string |  |
| `workAssignments[].assignmentStatus.reasonCode.longName` | string |  |
| `workAssignments[].assignmentStatus.statusCode.codeValue` | string |  |
| `workAssignments[].assignmentStatus.statusCode.longName` | string |  |
| `workAssignments[].assignmentStatus.statusCode.shortName` | string |  |
| `workAssignments[].baseRemuneration.annualRateAmount.amountValue` | number | Annual rate amount. |
| `workAssignments[].baseRemuneration.annualRateAmount.currencyCode` | string |  |
| `workAssignments[].baseRemuneration.annualRateAmount.nameCode.codeValue` | string |  |
| `workAssignments[].baseRemuneration.annualRateAmount.nameCode.shortName` | string |  |
| `workAssignments[].baseRemuneration.effectiveDate` | string |  |
| `workAssignments[].baseRemuneration.hourlyRateAmount.amountValue` | number | Hourly rate amount. |
| `workAssignments[].baseRemuneration.hourlyRateAmount.currencyCode` | string |  |
| `workAssignments[].baseRemuneration.hourlyRateAmount.nameCode.codeValue` | string |  |
| `workAssignments[].baseRemuneration.hourlyRateAmount.nameCode.shortName` | string |  |
| `workAssignments[].hireDate` | string |  |
| `workAssignments[].homeWorkLocation.address.cityName` | string |  |
| `workAssignments[].homeWorkLocation.address.countryCode` | string |  |
| `workAssignments[].homeWorkLocation.address.countrySubdivisionLevel1.codeValue` | string |  |
| `workAssignments[].homeWorkLocation.address.countrySubdivisionLevel1.shortName` | string |  |
| `workAssignments[].homeWorkLocation.address.countrySubdivisionLevel1.subdivisionType` | string |  |
| `workAssignments[].homeWorkLocation.address.lineOne` | string |  |
| `workAssignments[].homeWorkLocation.address.postalCode` | string |  |
| `workAssignments[].homeWorkLocation.nameCode.codeValue` | string |  |
| `workAssignments[].homeWorkLocation.nameCode.shortName` | string |  |
| `workAssignments[].itemID` | string |  |
| `workAssignments[].managementPositionIndicator` | boolean |  |
| `workAssignments[].payCycleCode.codeValue` | string |  |
| `workAssignments[].payCycleCode.shortName` | string |  |
| `workAssignments[].payrollFileNumber` | string |  |
| `workAssignments[].payrollGroupCode` | string |  |
| `workAssignments[].payrollProcessingStatusCode.shortName` | string |  |
| `workAssignments[].payrollScheduleGroupID` | string |  |
| `workAssignments[].positionID` | string |  |
| `workAssignments[].primaryIndicator` | boolean |  |
| `workAssignments[].seniorityDate` | string |  |
| `workAssignments[].terminationDate` | string |  |
| `workAssignments[].voluntaryIndicator` | boolean |  |
| `workAssignments[].workerTimeProfile.timeAndAttendanceIndicator` | boolean |  |
| `workerDates.originalHireDate` | string |  |
| `workerDates.terminationDate` | string |  |
| `workerID.idValue` | string |  |
| `workerStatus.statusCode.codeValue` | string |  |

## Native endpoint

Through the native ADP API, this operation is `GET hr/v2/workers` (base URL `https://api.adp.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-workers.md) for the provider-specific parameters and requirements.

