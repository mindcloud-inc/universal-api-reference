# BambooHR Universal API Examples

These examples use the MindCloud API key and BambooHR connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Employees

Retrieves a list of employees from BambooHR.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-employees?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-employees?${params}`, {
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

See the full [List Employees action reference](actions/list-employees.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bambooHrV2/latest/actions/list-employees).

## Add Time Off Request

Creates a time off request for an employee in BambooHR.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/add-time-off-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "employeeId": "4"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/add-time-off-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "employeeId": "4"
  })
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

See the full [Add Time Off Request action reference](actions/add-time-off-request.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bambooHrV2/latest/actions/add-time-off-request).
