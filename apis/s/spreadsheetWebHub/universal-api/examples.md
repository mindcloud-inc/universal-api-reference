# SpreadsheetWeb Hub Universal API Examples

These examples use the MindCloud API key and SpreadsheetWeb Hub connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Calculate Multiple

Performs multiple calculations in SpreadsheetWeb Hub.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/calculate-multiple?connectionId=$CONNECTION_ID&request.applicationId=string&request.workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "request.applicationId": "string",
  "request.workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/calculate-multiple?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Calculate Multiple action reference](actions/calculate-multiple.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/spreadsheetWebHub/latest/actions/calculate-multiple).

## Create Data Share Link

Creates a new data share link in SpreadsheetWeb Hub.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/create-data-share-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "request.applicationId": "string",
  "request.workspaceId": "string",
  "request.recordId": 1,
  "request.actionType": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/spreadsheetWebHub/latest/actions/create-data-share-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "request.applicationId": "string",
    "request.workspaceId": "string",
    "request.recordId": 1,
    "request.actionType": 1
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
      "accessedCount": 1,
      "actionType": 1,
      "applicationId": "string",
      "createdByClientId": 1,
      "createdByUserId": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "dataShareLinkId": "https://example.com",
      "dataShareToken": "string",
      "expirationTime": "2026-05-07T12:00:00.000Z",
      "modificationDate": "2026-05-07T12:00:00.000Z",
      "recordId": 1,
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Data Share Link action reference](actions/create-data-share-link.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/spreadsheetWebHub/latest/actions/create-data-share-link).
