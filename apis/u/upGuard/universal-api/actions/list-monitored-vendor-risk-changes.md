# UpGuard: List Monitored Vendor Risk Changes

Retrieves risk changes for monitored vendors in UpGuard.

```
GET https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-monitored-vendor-risk-changes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-monitored-vendor-risk-changes?connectionId=$CONNECTION_ID&limit=25&offset=0&startDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "startDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-monitored-vendor-risk-changes?${params}`, {
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
| `startDate` | string | yes | The RFC 3339 start date used to calculate introduced and resolved risks. |
| `endDate` | string | no | The RFC 3339 end date used to calculate introduced and resolved risks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "totalResults": 1,
      "vendors": [
        {
          "id": 1,
          "name": "Ava Chen",
          "primaryHostname": "Ava Chen",
          "risksIntroduced": [
            {
              "groupID": "string",
              "highestSeverity": 1,
              "highestSeverityName": "Ava Chen",
              "name": "Ava Chen",
              "risks": [
                {
                  "category": "string",
                  "description": "string",
                  "group": "string",
                  "id": "string",
                  "name": "Ava Chen",
                  "remediation": "string",
                  "riskDetails": "string",
                  "riskSubtype": "string",
                  "riskType": "string",
                  "scanDiffs": [
                    {
                      "expected": "string",
                      "hostname": "Ava Chen",
                      "property": "string",
                      "scanA": {
                        "date": "string",
                        "metaValue": "string",
                        "status": "string"
                      },
                      "scanB": {
                        "date": "string",
                        "metaValue": "string",
                        "status": "string"
                      }
                    }
                  ],
                  "severity": 1,
                  "severityName": "Ava Chen",
                  "vendorDiff": {}
                }
              ]
            }
          ],
          "risksResolved": [
            {
              "groupID": "string",
              "highestSeverity": 1,
              "highestSeverityName": "Ava Chen",
              "name": "Ava Chen",
              "risks": [
                {
                  "category": "string",
                  "description": "string",
                  "group": "string",
                  "id": "string",
                  "name": "Ava Chen",
                  "remediation": "string",
                  "riskDetails": "string",
                  "riskSubtype": "string",
                  "riskType": "string",
                  "scanDiffs": [
                    {
                      "expected": "string",
                      "hostname": "Ava Chen",
                      "property": "string",
                      "scanA": {
                        "date": "string",
                        "metaValue": "string",
                        "status": "string"
                      },
                      "scanB": {
                        "date": "string",
                        "metaValue": "string",
                        "status": "string"
                      }
                    }
                  ],
                  "severity": 1,
                  "severityName": "Ava Chen",
                  "vendorDiff": {}
                }
              ]
            }
          ]
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `totalResults` | number |  |
| `vendors[].id` | number |  |
| `vendors[].name` | string |  |
| `vendors[].primaryHostname` | string |  |
| `vendors[].risksIntroduced[].groupID` | string |  |
| `vendors[].risksIntroduced[].highestSeverity` | number |  |
| `vendors[].risksIntroduced[].highestSeverityName` | string |  |
| `vendors[].risksIntroduced[].name` | string |  |
| `vendors[].risksIntroduced[].risks[].category` | string |  |
| `vendors[].risksIntroduced[].risks[].description` | string |  |
| `vendors[].risksIntroduced[].risks[].group` | string |  |
| `vendors[].risksIntroduced[].risks[].id` | string |  |
| `vendors[].risksIntroduced[].risks[].name` | string |  |
| `vendors[].risksIntroduced[].risks[].remediation` | string |  |
| `vendors[].risksIntroduced[].risks[].riskDetails` | string |  |
| `vendors[].risksIntroduced[].risks[].riskSubtype` | string |  |
| `vendors[].risksIntroduced[].risks[].riskType` | string |  |
| `vendors[].risksIntroduced[].risks[].scanDiffs[].expected` | string |  |
| `vendors[].risksIntroduced[].risks[].scanDiffs[].hostname` | string |  |
| `vendors[].risksIntroduced[].risks[].scanDiffs[].property` | string |  |
| `vendors[].risksIntroduced[].risks[].scanDiffs[].scanA.date` | string |  |
| `vendors[].risksIntroduced[].risks[].scanDiffs[].scanA.metaValue` | string |  |
| `vendors[].risksIntroduced[].risks[].scanDiffs[].scanA.status` | string |  |
| `vendors[].risksIntroduced[].risks[].scanDiffs[].scanB.date` | string |  |
| `vendors[].risksIntroduced[].risks[].scanDiffs[].scanB.metaValue` | string |  |
| `vendors[].risksIntroduced[].risks[].scanDiffs[].scanB.status` | string |  |
| `vendors[].risksIntroduced[].risks[].severity` | number |  |
| `vendors[].risksIntroduced[].risks[].severityName` | string |  |
| `vendors[].risksIntroduced[].risks[].vendorDiff` | object |  |
| `vendors[].risksResolved[].groupID` | string |  |
| `vendors[].risksResolved[].highestSeverity` | number |  |
| `vendors[].risksResolved[].highestSeverityName` | string |  |
| `vendors[].risksResolved[].name` | string |  |
| `vendors[].risksResolved[].risks[].category` | string |  |
| `vendors[].risksResolved[].risks[].description` | string |  |
| `vendors[].risksResolved[].risks[].group` | string |  |
| `vendors[].risksResolved[].risks[].id` | string |  |
| `vendors[].risksResolved[].risks[].name` | string |  |
| `vendors[].risksResolved[].risks[].remediation` | string |  |
| `vendors[].risksResolved[].risks[].riskDetails` | string |  |
| `vendors[].risksResolved[].risks[].riskSubtype` | string |  |
| `vendors[].risksResolved[].risks[].riskType` | string |  |
| `vendors[].risksResolved[].risks[].scanDiffs[].expected` | string |  |
| `vendors[].risksResolved[].risks[].scanDiffs[].hostname` | string |  |
| `vendors[].risksResolved[].risks[].scanDiffs[].property` | string |  |
| `vendors[].risksResolved[].risks[].scanDiffs[].scanA.date` | string |  |
| `vendors[].risksResolved[].risks[].scanDiffs[].scanA.metaValue` | string |  |
| `vendors[].risksResolved[].risks[].scanDiffs[].scanA.status` | string |  |
| `vendors[].risksResolved[].risks[].scanDiffs[].scanB.date` | string |  |
| `vendors[].risksResolved[].risks[].scanDiffs[].scanB.metaValue` | string |  |
| `vendors[].risksResolved[].risks[].scanDiffs[].scanB.status` | string |  |
| `vendors[].risksResolved[].risks[].severity` | number |  |
| `vendors[].risksResolved[].risks[].severityName` | string |  |
| `vendors[].risksResolved[].risks[].vendorDiff` | object |  |

## Native endpoint

Through the native UpGuard API, this operation is `GET /risks/vendors/diffs` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-monitored-vendor-risk-changes.md) for the provider-specific parameters and requirements.

