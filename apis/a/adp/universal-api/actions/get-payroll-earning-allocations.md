# ADP: Get Payroll Earning Allocations



```
GET https://connect.mindcloud.co/v1/universal/adp/latest/actions/get-payroll-earning-allocations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ADP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adp/latest/actions/get-payroll-earning-allocations?connectionId=$CONNECTION_ID&outputId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "outputId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adp/latest/actions/get-payroll-earning-allocations?${params}`, {
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
| `outputId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alternateJobIDs": [
        {
          "idValue": "string",
          "schemeCode": {
            "shortName": "Ava Chen"
          }
        }
      ],
      "associatePayments": [
        {
          "associateOID": "string",
          "payments": [
            {
              "paymentAllocations": [
                {
                  "earnings": {
                    "earningsSections": [
                      {
                        "earningsItems": [
                          {
                            "configurationTags": [
                              {
                                "tagCode": "string",
                                "tagType": {
                                  "dataTypeCode": "string"
                                },
                                "tagValues": [
                                  "string"
                                ]
                              }
                            ],
                            "earningAmount": {
                              "amountValue": 1
                            },
                            "earningClassificationCode": {
                              "codeValue": "string",
                              "shortName": "Ava Chen"
                            },
                            "earningID": {
                              "idDescription": "string",
                              "idValue": "string"
                            },
                            "payRate": {
                              "baseUnitCode": {
                                "codeValue": "string",
                                "shortName": "Ava Chen"
                              },
                              "rateValue": 1
                            },
                            "timeWorkedQuantity": {
                              "quantityValue": 1,
                              "unitTimeCode": {
                                "codeValue": "string",
                                "shortName": "Ava Chen"
                              }
                            }
                          }
                        ]
                      }
                    ]
                  }
                }
              ]
            }
          ]
        }
      ],
      "itemID": "string",
      "payrollGroupCode": {
        "codeValue": "string",
        "shortName": "Ava Chen"
      },
      "payrollProcessingJobID": "string",
      "payrollProcessingJobStatusCode": {
        "codeValue": "string",
        "shortName": "Ava Chen"
      },
      "payrollRegionCode": {
        "codeValue": "string"
      },
      "payrollScheduleReference": {
        "payrollRunNumber": "string",
        "payrollScheduleID": "string",
        "payrollWeekNumber": "string",
        "payrollYear": "string",
        "scheduleEntryID": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alternateJobIDs[].idValue` | string |  |
| `alternateJobIDs[].schemeCode.shortName` | string |  |
| `associatePayments[].associateOID` | string |  |
| `associatePayments[].payments[].paymentAllocations[].earnings.earningsSections[].earningsItems[].configurationTags[].tagCode` | string |  |
| `associatePayments[].payments[].paymentAllocations[].earnings.earningsSections[].earningsItems[].configurationTags[].tagType.dataTypeCode` | string |  |
| `associatePayments[].payments[].paymentAllocations[].earnings.earningsSections[].earningsItems[].configurationTags[].tagValues[]` | string |  |
| `associatePayments[].payments[].paymentAllocations[].earnings.earningsSections[].earningsItems[].earningAmount.amountValue` | number |  |
| `associatePayments[].payments[].paymentAllocations[].earnings.earningsSections[].earningsItems[].earningClassificationCode.codeValue` | string |  |
| `associatePayments[].payments[].paymentAllocations[].earnings.earningsSections[].earningsItems[].earningClassificationCode.shortName` | string |  |
| `associatePayments[].payments[].paymentAllocations[].earnings.earningsSections[].earningsItems[].earningID.idDescription` | string |  |
| `associatePayments[].payments[].paymentAllocations[].earnings.earningsSections[].earningsItems[].earningID.idValue` | string |  |
| `associatePayments[].payments[].paymentAllocations[].earnings.earningsSections[].earningsItems[].payRate.baseUnitCode.codeValue` | string |  |
| `associatePayments[].payments[].paymentAllocations[].earnings.earningsSections[].earningsItems[].payRate.baseUnitCode.shortName` | string |  |
| `associatePayments[].payments[].paymentAllocations[].earnings.earningsSections[].earningsItems[].payRate.rateValue` | number |  |
| `associatePayments[].payments[].paymentAllocations[].earnings.earningsSections[].earningsItems[].timeWorkedQuantity.quantityValue` | number |  |
| `associatePayments[].payments[].paymentAllocations[].earnings.earningsSections[].earningsItems[].timeWorkedQuantity.unitTimeCode.codeValue` | string |  |
| `associatePayments[].payments[].paymentAllocations[].earnings.earningsSections[].earningsItems[].timeWorkedQuantity.unitTimeCode.shortName` | string |  |
| `itemID` | string |  |
| `payrollGroupCode.codeValue` | string |  |
| `payrollGroupCode.shortName` | string |  |
| `payrollProcessingJobID` | string |  |
| `payrollProcessingJobStatusCode.codeValue` | string |  |
| `payrollProcessingJobStatusCode.shortName` | string |  |
| `payrollRegionCode.codeValue` | string |  |
| `payrollScheduleReference.payrollRunNumber` | string |  |
| `payrollScheduleReference.payrollScheduleID` | string |  |
| `payrollScheduleReference.payrollWeekNumber` | string |  |
| `payrollScheduleReference.payrollYear` | string |  |
| `payrollScheduleReference.scheduleEntryID` | string |  |

## Native endpoint

Through the native ADP API, this operation is `GET payroll/v2/payroll-output/:outputId/associate-payment-allocations/earnings` (base URL `https://api.adp.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payroll-earning-allocations.md) for the provider-specific parameters and requirements.

