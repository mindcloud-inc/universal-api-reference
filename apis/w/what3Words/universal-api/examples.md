# What3Words Universal API Examples

These examples use the MindCloud API key and What3Words connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Available what3words Languages

Lists available what3words languages for 3 word addresses.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/what3Words/latest/actions/list-available-what3words-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/what3Words/latest/actions/list-available-what3words-languages?${params}`, {
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
      "code": "string",
      "locales": [
        {}
      ],
      "name": "Ava Chen",
      "nativeName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Available what3words Languages action reference](actions/list-available-what3words-languages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/what3Words/latest/actions/list-available-what3words-languages).
