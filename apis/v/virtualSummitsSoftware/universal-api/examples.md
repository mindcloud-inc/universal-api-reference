# Virtual Summits Software Universal API Examples

These examples use the MindCloud API key and Virtual Summits Software connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Summit Attendees



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/virtualSummitsSoftware/latest/actions/list-summit-attendees?connectionId=$CONNECTION_ID&summitId=4463" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "summitId": "4463"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/virtualSummitsSoftware/latest/actions/list-summit-attendees?${params}`, {
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

See the full [List Summit Attendees action reference](actions/list-summit-attendees.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/virtualSummitsSoftware/latest/actions/list-summit-attendees).
