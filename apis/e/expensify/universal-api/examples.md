# Expensify Universal API Examples

These examples use the MindCloud API key and Expensify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Policies

Retrieves policies from Expensify.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/expensify/latest/actions/list-policies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/expensify/latest/actions/list-policies?${params}`, {
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
      "approvalMode": "string",
      "created": "string",
      "id": "string",
      "name": "Ava Chen",
      "outputCurrency": "string",
      "owner": "string",
      "role": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Policies action reference](actions/list-policies.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/expensify/latest/actions/list-policies).

## Assign Employees To Domain Groups

Updates employee domain group assignments in Expensify.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/expensify/latest/actions/assign-employees-to-domain-groups" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "employeesJson": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/expensify/latest/actions/assign-employees-to-domain-groups', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "employeesJson": "string"
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
      "dry-run": true,
      "email": "ava@example.com",
      "reason": "string",
      "requestID": "string",
      "responseCode": 1,
      "updatedEmployeesCount": 1
    }
  ],
  "meta": {}
}
```

See the full [Assign Employees To Domain Groups action reference](actions/assign-employees-to-domain-groups.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/expensify/latest/actions/assign-employees-to-domain-groups).
