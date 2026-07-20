# Float Universal API Examples

These examples use the MindCloud API key and Float connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List People

Retrieves people from Float.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/float/latest/actions/list-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/float/latest/actions/list-people?${params}`, {
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
      "active": 1,
      "autoEmail": 1,
      "avatarFile": "string",
      "contractor": 1,
      "costRate": {},
      "created": {},
      "defaultHourlyRate": {},
      "department": {},
      "email": "ava@example.com",
      "employeeType": 1,
      "endDate": {},
      "jobTitle": {},
      "modified": "string",
      "name": "Ava Chen",
      "nonWorkDays": {},
      "notes": {},
      "peopleId": 1,
      "peopleTypeId": 1,
      "regionId": 1,
      "roleId": {},
      "startDate": "string",
      "workDaysHours": {},
      "workDaysHoursHistory": {}
    }
  ],
  "meta": {}
}
```

See the full [List People action reference](actions/list-people.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/float/latest/actions/list-people).

## Create Allocation

Creates a new allocation in Float.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/float/latest/actions/create-allocation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "startDate": "string",
  "endDate": "string",
  "hours": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/float/latest/actions/create-allocation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "startDate": "string",
    "endDate": "string",
    "hours": 1
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
      "billable": 1,
      "created": "string",
      "createdBy": 1,
      "endDate": "string",
      "hours": 1,
      "modified": "string",
      "modifiedBy": 1,
      "name": "Ava Chen",
      "notes": {},
      "parentTaskId": {},
      "peopleId": 1,
      "phaseId": 1,
      "projectId": 1,
      "repeatEndDate": {},
      "repeatState": 1,
      "rootTaskId": {},
      "startDate": "string",
      "startTime": {},
      "status": 1,
      "taskId": 1,
      "taskMetaId": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Allocation action reference](actions/create-allocation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/float/latest/actions/create-allocation).
