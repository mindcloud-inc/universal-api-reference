# Wodely Universal API Examples

These examples use the MindCloud API key and Wodely connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Drivers



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wodely/latest/actions/list-drivers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wodely/latest/actions/list-drivers?${params}`, {
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
      "address": "string",
      "businessNumber": "string",
      "capacity": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "isOnDuty": 1,
      "lastName": "Chen",
      "numActiveTask": 1,
      "phoneNumber": "string",
      "position": "string",
      "profileImage": "string",
      "skills": "string",
      "statusDesc": "string",
      "statusId": 1,
      "teamName": "Ava Chen",
      "telephone": "string",
      "timeZone": "string",
      "transportDesc": "string",
      "transportLicensePlate": "string",
      "transportTypeId": 1,
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Drivers action reference](actions/list-drivers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wodely/latest/actions/list-drivers).

## Assign Tasks to Driver in Batch



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wodely/latest/actions/assign-tasks-to-driver-in-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assignments[].taskGuid": "DD2A6408A6",
  "assignments[].driverUserId": "driver@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wodely/latest/actions/assign-tasks-to-driver-in-batch', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assignments[].taskGuid": "DD2A6408A6",
    "assignments[].driverUserId": "driver@example.com"
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
      "data": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Assign Tasks to Driver in Batch action reference](actions/assign-tasks-to-driver-in-batch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wodely/latest/actions/assign-tasks-to-driver-in-batch).
