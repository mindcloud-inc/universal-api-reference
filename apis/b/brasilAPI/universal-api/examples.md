# Brasil API Universal API Examples

These examples use the MindCloud API key and Brasil API connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Banks

Retrieves Brazilian banks from Brasil API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-banks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-banks?${params}`, {
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
      "code": 1,
      "fullName": "Ava Chen",
      "ispb": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Banks action reference](actions/list-banks.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/brasilAPI/latest/actions/list-banks).
