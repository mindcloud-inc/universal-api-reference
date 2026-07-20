# eCFR Universal API Examples

These examples use the MindCloud API key and eCFR connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Titles

Retrieves a list of titles from eCFR.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/list-titles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/list-titles?${params}`, {
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
      "meta": {},
      "titles": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Titles action reference](actions/list-titles.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eCFR/latest/actions/list-titles).
