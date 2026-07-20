# Department of Agriculture Universal API Examples

These examples use the MindCloud API key and Department of Agriculture connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List ARMS States

Retrieves ARMS states from Department of Agriculture.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/list-arms-states?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/list-arms-states?${params}`, {
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
      "code": "string",
      "id": "string",
      "name": "Ava Chen",
      "terms": "string"
    }
  ],
  "meta": {}
}
```

See the full [List ARMS States action reference](actions/list-arms-states.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/departmentOfAgriculture/latest/actions/list-arms-states).
