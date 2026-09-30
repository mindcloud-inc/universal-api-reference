# File Converter Universal API Examples

These examples use the MindCloud API key and File Converter connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Convert File

Convert a file to a specific format

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fileConverter/latest/actions/convert-file?connectionId=$CONNECTION_ID&file=string&outputFormat=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file": "string",
  "outputFormat": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fileConverter/latest/actions/convert-file?${params}`, {
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

See the full [Convert File action reference](actions/convert-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fileConverter/latest/actions/convert-file).
