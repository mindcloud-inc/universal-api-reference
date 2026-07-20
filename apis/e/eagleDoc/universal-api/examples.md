# Eagle Doc Universal API Examples

These examples use the MindCloud API key and Eagle Doc connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Month Usage

Retrieves current month usage from Eagle Doc.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/get-current-month-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/get-current-month-usage?${params}`, {
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
      "contractQuota": 1,
      "currentMonth": "string",
      "endedAt": "2026-05-07T12:00:00.000Z",
      "hardLimit": 1,
      "overUsage": 1,
      "overUsageAllowed": true,
      "overUsageCost": 1,
      "pricePerPageOverUsage": 1,
      "quotaUsed": 1,
      "startedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get Current Month Usage action reference](actions/get-current-month-usage.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eagleDoc/latest/actions/get-current-month-usage).

## Create Any Document Batch OCR Task

Creates an any-document batch OCR task in Eagle Doc.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/create-any-document-batch-ocr-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/create-any-document-batch-ocr-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
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
      "createdTime": "2026-05-07T12:00:00.000Z",
      "finishedTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "messages": {},
      "numberOfFiles": 1,
      "numberOfPages": 1,
      "originalFileNames": [
        "Ava Chen"
      ],
      "queryParams": {
        "configId": "string",
        "docType": "string",
        "endPoint": "string",
        "fromDashboardSaveResult": "string",
        "privacy": "string"
      },
      "status": "string",
      "taskType": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Any Document Batch OCR Task action reference](actions/create-any-document-batch-ocr-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eagleDoc/latest/actions/create-any-document-batch-ocr-task).
