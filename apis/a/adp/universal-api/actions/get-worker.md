# ADP: Get Worker



```
GET https://connect.mindcloud.co/v1/universal/adp/latest/actions/get-worker
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ADP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adp/latest/actions/get-worker?connectionId=$CONNECTION_ID&aOid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "aOid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adp/latest/actions/get-worker?${params}`, {
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
| `aOid` | string | yes |  |
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "associateOID": "string",
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
              "shortName": "Ava Chen"
            }
          }
        ],
        "numberFields": [
          {
            "itemID": "string",
            "nameCode": {
              "codeValue": "Ava Chen",
              "shortName": "Ava Chen"
            }
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
        "birthDate": "2026-05-07T12:00:00.000Z",
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
          ],
          "mobiles": [
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
          "givenName": "Ava Chen",
          "middleName": "Ava Chen"
        },
        "maritalStatusCode": {
          "codeValue": "string",
          "shortName": "Ava Chen"
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
          "assignedWorkLocations": [
            {
              "address": {
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
              }
            }
          ],
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
              "currencyCode": "string",
              "nameCode": {
                "codeValue": "Ava Chen",
                "shortName": "Ava Chen"
              }
            },
            "effectiveDate": "string",
            "hourlyRateAmount": {
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
          "industryClassifications": [
            {
              "classificationCode": {
                "codeValue": "string",
                "shortName": "Ava Chen"
              },
              "nameCode": {
                "codeValue": "Ava Chen",
                "shortName": "Ava Chen"
              }
            }
          ],
          "itemID": "string",
          "jobCode": {
            "codeValue": "string",
            "shortName": "Ava Chen"
          },
          "jobFunctionCode": {
            "codeValue": "string",
            "shortName": "Ava Chen"
          },
          "jobTitle": "string",
          "managementPositionIndicator": true,
          "occupationalClassifications": [
            {
              "classificationCode": {
                "codeValue": "string",
                "shortName": "Ava Chen"
              },
              "nameCode": {
                "codeValue": "Ava Chen",
                "shortName": "Ava Chen"
              }
            }
          ],
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
          "wageLawCoverage": {
            "coverageCode": {
              "codeValue": "string",
              "shortName": "Ava Chen"
            },
            "wageLawNameCode": {
              "codeValue": "Ava Chen",
              "longName": "Ava Chen"
            }
          },
          "workerTimeProfile": {
            "timeAndAttendanceIndicator": true
          }
        }
      ],
      "workerDates": {
        "originalHireDate": "2026-05-07T12:00:00.000Z",
        "terminationDate": "2026-05-07T12:00:00.000Z"
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
| `customFieldGroup.codeFields[].itemID` | string |  |
| `customFieldGroup.codeFields[].nameCode.codeValue` | string |  |
| `customFieldGroup.codeFields[].nameCode.shortName` | string |  |
| `customFieldGroup.dateFields[].itemID` | string |  |
| `customFieldGroup.dateFields[].nameCode.codeValue` | string |  |
| `customFieldGroup.dateFields[].nameCode.longName` | string |  |
| `customFieldGroup.indicatorFields[].itemID` | string |  |
| `customFieldGroup.indicatorFields[].nameCode.codeValue` | string |  |
| `customFieldGroup.indicatorFields[].nameCode.shortName` | string |  |
| `customFieldGroup.numberFields[].itemID` | string |  |
| `customFieldGroup.numberFields[].nameCode.codeValue` | string |  |
| `customFieldGroup.numberFields[].nameCode.shortName` | string |  |
| `customFieldGroup.percentFields[].itemID` | string |  |
| `customFieldGroup.percentFields[].nameCode.codeValue` | string |  |
| `customFieldGroup.percentFields[].nameCode.shortName` | string |  |
| `customFieldGroup.stringFields[].itemID` | string |  |
| `customFieldGroup.stringFields[].nameCode.codeValue` | string |  |
| `customFieldGroup.stringFields[].nameCode.longName` | string |  |
| `customFieldGroup.stringFields[].stringValue` | string |  |
| `person.birthDate` | date |  |
| `person.communication.landlines[].access` | string |  |
| `person.communication.landlines[].areaDialing` | string |  |
| `person.communication.landlines[].countryDialing` | string |  |
| `person.communication.landlines[].dialNumber` | string |  |
| `person.communication.landlines[].formattedNumber` | string |  |
| `person.communication.landlines[].itemID` | string |  |
| `person.communication.landlines[].nameCode.codeValue` | string |  |
| `person.communication.landlines[].nameCode.shortName` | string |  |
| `person.communication.mobiles[].access` | string |  |
| `person.communication.mobiles[].areaDialing` | string |  |
| `person.communication.mobiles[].countryDialing` | string |  |
| `person.communication.mobiles[].dialNumber` | string |  |
| `person.communication.mobiles[].formattedNumber` | string |  |
| `person.communication.mobiles[].itemID` | string |  |
| `person.communication.mobiles[].nameCode.codeValue` | string |  |
| `person.communication.mobiles[].nameCode.shortName` | string |  |
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
| `person.legalName.middleName` | string |  |
| `person.maritalStatusCode.codeValue` | string |  |
| `person.maritalStatusCode.shortName` | string |  |
| `person.raceCode.codeValue` | string |  |
| `person.raceCode.longName` | string |  |
| `person.raceCode.shortName` | string |  |
| `person.tobaccoUserIndicator` | boolean |  |
| `workAssignments[].actualStartDate` | string |  |
| `workAssignments[].assignedWorkLocations[].address.cityName` | string |  |
| `workAssignments[].assignedWorkLocations[].address.countryCode` | string |  |
| `workAssignments[].assignedWorkLocations[].address.countrySubdivisionLevel1.codeValue` | string |  |
| `workAssignments[].assignedWorkLocations[].address.countrySubdivisionLevel1.shortName` | string |  |
| `workAssignments[].assignedWorkLocations[].address.countrySubdivisionLevel1.subdivisionType` | string |  |
| `workAssignments[].assignedWorkLocations[].address.lineOne` | string |  |
| `workAssignments[].assignedWorkLocations[].address.nameCode.codeValue` | string |  |
| `workAssignments[].assignedWorkLocations[].address.nameCode.longName` | string |  |
| `workAssignments[].assignedWorkLocations[].address.nameCode.shortName` | string |  |
| `workAssignments[].assignedWorkLocations[].address.postalCode` | string |  |
| `workAssignments[].assignmentStatus.effectiveDate` | string |  |
| `workAssignments[].assignmentStatus.reasonCode.codeValue` | string |  |
| `workAssignments[].assignmentStatus.reasonCode.longName` | string |  |
| `workAssignments[].assignmentStatus.statusCode.codeValue` | string |  |
| `workAssignments[].assignmentStatus.statusCode.longName` | string |  |
| `workAssignments[].assignmentStatus.statusCode.shortName` | string |  |
| `workAssignments[].baseRemuneration.annualRateAmount.currencyCode` | string |  |
| `workAssignments[].baseRemuneration.annualRateAmount.nameCode.codeValue` | string |  |
| `workAssignments[].baseRemuneration.annualRateAmount.nameCode.shortName` | string |  |
| `workAssignments[].baseRemuneration.effectiveDate` | string |  |
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
| `workAssignments[].industryClassifications[].classificationCode.codeValue` | string |  |
| `workAssignments[].industryClassifications[].classificationCode.shortName` | string |  |
| `workAssignments[].industryClassifications[].nameCode.codeValue` | string |  |
| `workAssignments[].industryClassifications[].nameCode.shortName` | string |  |
| `workAssignments[].itemID` | string |  |
| `workAssignments[].jobCode.codeValue` | string |  |
| `workAssignments[].jobCode.shortName` | string |  |
| `workAssignments[].jobFunctionCode.codeValue` | string |  |
| `workAssignments[].jobFunctionCode.shortName` | string |  |
| `workAssignments[].jobTitle` | string |  |
| `workAssignments[].managementPositionIndicator` | boolean |  |
| `workAssignments[].occupationalClassifications[].classificationCode.codeValue` | string |  |
| `workAssignments[].occupationalClassifications[].classificationCode.shortName` | string |  |
| `workAssignments[].occupationalClassifications[].nameCode.codeValue` | string |  |
| `workAssignments[].occupationalClassifications[].nameCode.shortName` | string |  |
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
| `workAssignments[].wageLawCoverage.coverageCode.codeValue` | string |  |
| `workAssignments[].wageLawCoverage.coverageCode.shortName` | string |  |
| `workAssignments[].wageLawCoverage.wageLawNameCode.codeValue` | string |  |
| `workAssignments[].wageLawCoverage.wageLawNameCode.longName` | string |  |
| `workAssignments[].workerTimeProfile.timeAndAttendanceIndicator` | boolean |  |
| `workerDates.originalHireDate` | date |  |
| `workerDates.terminationDate` | date |  |
| `workerID.idValue` | string |  |
| `workerStatus.statusCode.codeValue` | string |  |

## Native endpoint

Through the native ADP API, this operation is `GET hr/v2/workers/:aOid` (base URL `https://api.adp.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-worker.md) for the provider-specific parameters and requirements.

