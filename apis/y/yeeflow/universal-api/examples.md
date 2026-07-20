# Yeeflow Universal API Examples

These examples use the MindCloud API key and Yeeflow connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Departments



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yeeflow/latest/actions/list-departments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yeeflow/latest/actions/list-departments?${params}`, {
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
      "Data": [
        "string"
      ],
      "Message": "string",
      "Status": 1,
      "TotalCount": 1
    }
  ],
  "meta": {}
}
```

See the full [List Departments action reference](actions/list-departments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/yeeflow/latest/actions/list-departments).

## Add Users To Group



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/yeeflow/latest/actions/add-users-to-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yeeflow/latest/actions/add-users-to-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "Data": "string",
      "Message": "string",
      "Status": 1,
      "TotalCount": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Users To Group action reference](actions/add-users-to-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/yeeflow/latest/actions/add-users-to-group).
