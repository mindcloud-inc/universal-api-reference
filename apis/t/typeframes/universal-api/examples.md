# Typeframes Universal API Examples

These examples use the MindCloud API key and Typeframes connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Projects

Retrieves recent video projects from Typeframes.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typeframes/latest/actions/get-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typeframes/latest/actions/get-projects?${params}`, {
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

See the full [Get Projects action reference](actions/get-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/typeframes/latest/actions/get-projects).
