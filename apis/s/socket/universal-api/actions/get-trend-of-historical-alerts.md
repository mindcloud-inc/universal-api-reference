# Socket: Get Trend of Historical Alerts

Retrieves historical alert trends from Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-trend-of-historical-alerts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-trend-of-historical-alerts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-trend-of-historical-alerts?${params}`, {
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
      "items": [
        {
          "dataPoints": [
            {}
          ],
          "date": "string",
          "startOfDayTimestamp": 1
        }
      ],
      "meta": {
        "aggregation": {
          "fields": [
            "string"
          ],
          "groups": [
            [
              "string"
            ]
          ]
        },
        "endDateInclusive": "string",
        "filters": {
          "alertAction": {
            "notIn": [
              "string"
            ]
          },
          "alertActionSourceType": {
            "notIn": [
              "string"
            ]
          },
          "alertCategory": {
            "notIn": [
              "string"
            ]
          },
          "alertCveId": {
            "notIn": [
              "string"
            ]
          },
          "alertCveTitle": {
            "notIn": [
              "string"
            ]
          },
          "alertCweId": {
            "notIn": [
              "string"
            ]
          },
          "alertCweName": {
            "notIn": [
              "Ava Chen"
            ]
          },
          "alertEPSS": {
            "notIn": [
              "string"
            ]
          },
          "alertFixType": {
            "notIn": [
              "string"
            ]
          },
          "alertKEV": [
            true
          ],
          "alertPriority": {
            "notIn": [
              "string"
            ]
          },
          "alertReachabilityAnalysisType": {
            "notIn": [
              "string"
            ]
          },
          "alertReachabilityType": {
            "notIn": [
              "string"
            ]
          },
          "alertSeverity": {
            "notIn": [
              "string"
            ]
          },
          "alertType": {
            "notIn": [
              "string"
            ]
          },
          "artifactName": {
            "notIn": [
              "Ava Chen"
            ]
          },
          "artifactType": {
            "notIn": [
              "string"
            ]
          },
          "branch": {
            "notIn": [
              "string"
            ]
          },
          "cvePatchStatus": {
            "notIn": [
              "string"
            ]
          },
          "dependencyDead": [
            true
          ],
          "dependencyDev": [
            true
          ],
          "dependencyDirect": [
            true
          ],
          "repoFullName": {
            "notIn": [
              "Ava Chen"
            ]
          },
          "repoLabels": {
            "notIn": [
              "string"
            ]
          },
          "repoSlug": {
            "notIn": [
              "string"
            ]
          }
        },
        "interval": "string",
        "organizationId": "string",
        "startDateInclusive": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `items[]` | object |  |
| `items[].dataPoints` | array<object> |  |
| `items[].dataPoints[]` | object |  |
| `items[].date` | string |  |
| `items[].startOfDayTimestamp` | number |  |
| `meta` | object |  |
| `meta.aggregation` | object |  |
| `meta.aggregation.fields` | array<string> |  |
| `meta.aggregation.groups` | array<array> |  |
| `meta.aggregation.groups[]` | array |  |
| `meta.endDateInclusive` | string |  |
| `meta.filters` | object |  |
| `meta.filters.alertAction` | array<string> |  |
| `meta.filters.alertAction.notIn` | array<string> |  |
| `meta.filters.alertActionSourceType` | array<string> |  |
| `meta.filters.alertActionSourceType.notIn` | array<string> |  |
| `meta.filters.alertCategory` | array<string> |  |
| `meta.filters.alertCategory.notIn` | array<string> |  |
| `meta.filters.alertCveId` | array<string> |  |
| `meta.filters.alertCveId.notIn` | array<string> |  |
| `meta.filters.alertCveTitle` | array<string> |  |
| `meta.filters.alertCveTitle.notIn` | array<string> |  |
| `meta.filters.alertCweId` | array<string> |  |
| `meta.filters.alertCweId.notIn` | array<string> |  |
| `meta.filters.alertCweName` | array<string> |  |
| `meta.filters.alertCweName.notIn` | array<string> |  |
| `meta.filters.alertEPSS` | array<string> |  |
| `meta.filters.alertEPSS.notIn` | array<string> |  |
| `meta.filters.alertFixType` | array<string> |  |
| `meta.filters.alertFixType.notIn` | array<string> |  |
| `meta.filters.alertKEV` | array<boolean> |  |
| `meta.filters.alertPriority` | array<string> |  |
| `meta.filters.alertPriority.notIn` | array<string> |  |
| `meta.filters.alertReachabilityAnalysisType` | array<string> |  |
| `meta.filters.alertReachabilityAnalysisType.notIn` | array<string> |  |
| `meta.filters.alertReachabilityType` | array<string> |  |
| `meta.filters.alertReachabilityType.notIn` | array<string> |  |
| `meta.filters.alertSeverity` | array<string> |  |
| `meta.filters.alertSeverity.notIn` | array<string> |  |
| `meta.filters.alertType` | array<string> |  |
| `meta.filters.alertType.notIn` | array<string> |  |
| `meta.filters.artifactName` | array<string> |  |
| `meta.filters.artifactName.notIn` | array<string> |  |
| `meta.filters.artifactType` | array<string> |  |
| `meta.filters.artifactType.notIn` | array<string> |  |
| `meta.filters.branch` | array<string> |  |
| `meta.filters.branch.notIn` | array<string> |  |
| `meta.filters.cvePatchStatus` | array<string> |  |
| `meta.filters.cvePatchStatus.notIn` | array<string> |  |
| `meta.filters.dependencyDead` | array<boolean> |  |
| `meta.filters.dependencyDev` | array<boolean> |  |
| `meta.filters.dependencyDirect` | array<boolean> |  |
| `meta.filters.repoFullName` | array<string> |  |
| `meta.filters.repoFullName.notIn` | array<string> |  |
| `meta.filters.repoLabels` | array<string> |  |
| `meta.filters.repoLabels.notIn` | array<string> |  |
| `meta.filters.repoSlug` | array<string> |  |
| `meta.filters.repoSlug.notIn` | array<string> |  |
| `meta.interval` | string |  |
| `meta.organizationId` | string |  |
| `meta.startDateInclusive` | string |  |

## Native endpoint

Through the native Socket API, this operation is `GET /orgs/:org_slug/historical/alerts/trend` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-trend-of-historical-alerts.md) for the provider-specific parameters and requirements.

