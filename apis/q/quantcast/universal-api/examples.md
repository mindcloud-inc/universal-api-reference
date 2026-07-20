# Quantcast Universal API Examples

These examples use the MindCloud API key and Quantcast connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Organizations

Retrieves organizations from Quantcast.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/list-organizations?${params}`, {
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
      "organizations": {
        "edges": {
          "id": 1,
          "name": "Ava Chen"
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [List Organizations action reference](actions/list-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quantcast/latest/actions/list-organizations).

## Request Async Attributed Actions Report

Requests an async attributed actions report from Quantcast.

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

Example response:

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

See the full [Request Async Attributed Actions Report action reference](actions/request-async-attributed-actions-report.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quantcast/latest/actions/request-async-attributed-actions-report).
