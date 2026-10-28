# UKG Ready Universal API Examples

These examples use the MindCloud API key and UKG Ready connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Employees



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uKGReady/latest/actions/list-employees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uKGReady/latest/actions/list-employees?${params}`, {
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

See the full [List Employees action reference](actions/list-employees.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uKGReady/latest/actions/list-employees).

## Create Time Punches



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uKGReady/latest/actions/create-time-punches" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "punches[].timestamp": "2026-05-07T12:00:00.000Z",
  "punches[].raw_type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uKGReady/latest/actions/create-time-punches', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "punches[].timestamp": "2026-05-07T12:00:00.000Z",
    "punches[].raw_type": "string"
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
      "employee": {
        "accountId": 1
      },
      "endDate": "string",
      "startDate": "string",
      "timeEntries": [
        {
          "approvalStatus": "string",
          "calcTotal": 1,
          "costCenters": [
            {
              "index": 1,
              "value": {
                "id": 1
              }
            }
          ],
          "date": "string",
          "id": 1,
          "isCalc": true,
          "isRaw": true,
          "total": 1,
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Time Punches action reference](actions/create-time-punches.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uKGReady/latest/actions/create-time-punches).
