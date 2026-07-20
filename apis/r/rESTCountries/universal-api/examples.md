# REST Countries Universal API Examples

These examples use the MindCloud API key and REST Countries connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Country Names and Flags



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rESTCountries/latest/actions/list-country-names-and-flags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rESTCountries/latest/actions/list-country-names-and-flags?${params}`, {
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
      "cca2": "string",
      "cca3": "string",
      "flags": {
        "alt": "string",
        "png": "string",
        "svg": "string"
      },
      "name": {
        "common": "Ava Chen",
        "official": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

See the full [List Country Names and Flags action reference](actions/list-country-names-and-flags.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rESTCountries/latest/actions/list-country-names-and-flags).
