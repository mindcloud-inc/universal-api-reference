# ProBackup Universal API Examples

These examples use the MindCloud API key and ProBackup connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Platforms

Retrieves active backup platforms from ProBackup.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proBackup/latest/actions/list-platforms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proBackup/latest/actions/list-platforms?${params}`, {
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
      "platforms": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Platforms action reference](actions/list-platforms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/proBackup/latest/actions/list-platforms).
