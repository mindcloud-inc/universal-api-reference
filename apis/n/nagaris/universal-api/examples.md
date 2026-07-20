# Nagaris Universal API Examples

These examples use the MindCloud API key and Nagaris connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Client Groups

Finds client groups in Nagaris by filters.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nagaris/latest/actions/list-client-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nagaris/latest/actions/list-client-groups?${params}`, {
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

See the full [List Client Groups action reference](actions/list-client-groups.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nagaris/latest/actions/list-client-groups).
