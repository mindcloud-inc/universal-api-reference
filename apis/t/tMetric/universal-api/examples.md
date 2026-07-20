# TMetric Universal API Examples

These examples use the MindCloud API key and TMetric connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/get-current-user?${params}`, {
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
      "accounts": [
        {
          "activity": {
            "blurScreenshots": true,
            "captureActivityLevels": true,
            "captureActivityLine": true,
            "captureAppsAndSites": true,
            "captureDetails": true,
            "captureScreenshots": true,
            "inactivityStopMinutes": 1
          },
          "firstWeekDay": 1,
          "id": 1,
          "name": "Ava Chen",
          "role": "string",
          "timeTracking": {
            "allowManualEditing": true,
            "allowNewClient": true,
            "allowNewProject": true,
            "allowNewTags": true,
            "allowNewTask": true,
            "allowTeamView": true,
            "requireDescription": true,
            "requireProject": true,
            "requireTags": true,
            "requireTask": true
          }
        }
      ],
      "activeAccountId": 1,
      "cultureInfo": {
        "id": "string",
        "nativeName": "Ava Chen"
      },
      "dateFormat": "string",
      "email": "ava@example.com",
      "iconUrl": "https://example.com",
      "id": 1,
      "name": "Ava Chen",
      "timeFormat": "string",
      "timeZone": {
        "currentOffset": 1,
        "displayName": "Ava Chen",
        "id": "string",
        "summerOffset": 1,
        "winterOffset": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tMetric/latest/actions/get-current-user).

## Add Time Entry Break



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/add-time-entry-break" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/add-time-entry-break', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1
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
      "endTime": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isBillable": true,
      "isInvoiced": true,
      "note": "string",
      "project": {
        "iconUrl": "https://example.com",
        "id": 1,
        "invoiceMethod": "string",
        "isBillable": true,
        "name": "Ava Chen",
        "status": "string"
      },
      "startTime": "2026-05-07T12:00:00.000Z",
      "task": {
        "id": 1,
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

See the full [Add Time Entry Break action reference](actions/add-time-entry-break.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tMetric/latest/actions/add-time-entry-break).
