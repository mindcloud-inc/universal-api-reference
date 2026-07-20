# Groopit Universal API Examples

These examples use the MindCloud API key and Groopit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Assignments



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/groopit/latest/actions/list-assignments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/groopit/latest/actions/list-assignments?${params}`, {
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
      "Id": "string",
      "Title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Assignments action reference](actions/list-assignments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/groopit/latest/actions/list-assignments).
