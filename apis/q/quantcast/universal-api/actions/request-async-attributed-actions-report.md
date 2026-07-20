# Quantcast: Request Async Attributed Actions Report

Requests an async attributed actions report from Quantcast.

```
POST https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/request-async-attributed-actions-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quantcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/request-async-attributed-actions-report" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "attributedActionsReportRequest": "{entity:{type:ACCOUNT,id:9974296},dateRange:{absoluteDateRange:{startDate:\"2026-04-01\",endDate:\"2026-04-07\"},timezone:\"UTC\"},campaignIds:[],adsetIds:[]}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/request-async-attributed-actions-report', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "attributedActionsReportRequest": "{entity:{type:ACCOUNT,id:9974296},dateRange:{absoluteDateRange:{startDate:\"2026-04-01\",endDate:\"2026-04-07\"},timezone:\"UTC\"},campaignIds:[],adsetIds:[]}"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attributedActionsReportRequest` | string | yes | GraphQL input object literal for the async attributed actions report request. Default: `{entity:{type:ACCOUNT,id:9974296},dateRange:{absoluteDateRange:{startDate:\"2026-04-01\",endDate:\"2026-04-07\"},timezone:\"UTC\"},campaignIds:[],adsetIds:[]}`. |
| `fileName` | string | no | Optional filename for the exported report. Default: `quantcast-attributed-actions-report.csv`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asyncAttributedActionsReport": {
        "reportRequestId": 1,
        "request": {
          "fileName": "Ava Chen"
        },
        "status": "string",
        "warningMessage": [
          "string"
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asyncAttributedActionsReport` | object | Async attributed actions report request accepted by Quantcast. |
| `asyncAttributedActionsReport.reportRequestId` | number | Async attributed actions report identifier. |
| `asyncAttributedActionsReport.request` | object | Original async attributed actions request metadata. |
| `asyncAttributedActionsReport.request.fileName` | string | Requested output file name. |
| `asyncAttributedActionsReport.status` | string | Current status of the async attributed actions report request. |
| `asyncAttributedActionsReport.warningMessage` | array<string> | Warning messages returned by Quantcast. |

## Native endpoint

Through the native Quantcast API, this operation is `GET /api/v2/graphql` (base URL `https://developers.quantcast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-async-attributed-actions-report.md) for the provider-specific parameters and requirements.

