# Priority Universal API Examples

These examples use the MindCloud API key and Priority connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Priority Version

Retrieves the Priority version.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-priority-version?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-priority-version?${params}`, {
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Priority Version action reference](actions/get-priority-version.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/priority/latest/actions/get-priority-version).
