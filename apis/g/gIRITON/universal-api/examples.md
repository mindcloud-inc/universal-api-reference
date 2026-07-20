# GIRITON Universal API Examples

These examples use the MindCloud API key and GIRITON connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Attendance Activities

Retrieves available attendance activities from GIRITON.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-attendance-activities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-attendance-activities?${params}`, {
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
      "canBePlanned": true,
      "canBeRequested": true,
      "color": "string",
      "counted": true,
      "dailyDataType": "string",
      "dataType": "string",
      "departments": [
        {}
      ],
      "description": "string",
      "displayStart": true,
      "displayStop": true,
      "entryTimestamp": "2026-05-07T12:00:00.000Z",
      "guid": "string",
      "id": "string",
      "mark": "string",
      "monthlyDataType": "string",
      "name": "Ava Chen",
      "number": "string",
      "renamedStart": "Ava Chen",
      "renamedStop": "Ava Chen",
      "selectStartTimes": [
        "string"
      ],
      "selectStopTimes": [
        "string"
      ],
      "shortcut": "string",
      "startColor": "string",
      "startIcon": "string",
      "stopColor": "string",
      "stopIcon": "string",
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Attendance Activities action reference](actions/list-attendance-activities.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gIRITON/latest/actions/list-attendance-activities).

## Add Vacation

Creates a new vacation entry in GIRITON.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/add-vacation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dateFrom": "string",
  "dateTo": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/add-vacation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dateFrom": "string",
    "dateTo": "string"
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
      "count": 1,
      "entries": [
        {}
      ],
      "newestTimestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Add Vacation action reference](actions/add-vacation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gIRITON/latest/actions/add-vacation).
