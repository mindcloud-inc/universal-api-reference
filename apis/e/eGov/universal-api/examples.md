# e-Gov Universal API Examples

These examples use the MindCloud API key and e-Gov connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Autocomplete Datasets

Finds datasets in e-Gov by partial name.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGov/latest/actions/autocomplete-datasets?connectionId=$CONNECTION_ID&q=%E4%BA%A4%E9%80%9A" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "交通"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGov/latest/actions/autocomplete-datasets?${params}`, {
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
      "match_displayed": "string",
      "match_field": "string",
      "name": "Ava Chen",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Autocomplete Datasets action reference](actions/autocomplete-datasets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eGov/latest/actions/autocomplete-datasets).
