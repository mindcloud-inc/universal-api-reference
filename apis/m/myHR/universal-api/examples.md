# MyHR Universal API Examples

These examples use the MindCloud API key and MyHR connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Employment Statuses



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myHR/latest/actions/list-employment-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myHR/latest/actions/list-employment-statuses?${params}`, {
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
      "id": "string",
      "label": "string",
      "object": "string",
      "tag": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Employment Statuses action reference](actions/list-employment-statuses.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/myHR/latest/actions/list-employment-statuses).

## Activate Employee



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/myHR/latest/actions/activate-employee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dateEffective": "string",
  "employeePid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/myHR/latest/actions/activate-employee', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dateEffective": "string",
    "employeePid": "string"
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
      "comment": "string",
      "dateCreation": "string",
      "dateEffective": "string",
      "dateLastAction": "string",
      "object": "string",
      "pid": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Activate Employee action reference](actions/activate-employee.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/myHR/latest/actions/activate-employee).
