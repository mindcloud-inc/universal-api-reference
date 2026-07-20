# Informizely Universal API Examples

These examples use the MindCloud API key and Informizely connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Sites



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/informizely/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/informizely/latest/actions/list-sites?${params}`, {
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
      "Domain": "string",
      "Id": "string",
      "Surveys": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Sites action reference](actions/list-sites.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/informizely/latest/actions/list-sites).
