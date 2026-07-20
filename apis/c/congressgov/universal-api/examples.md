# Congress.gov Universal API Examples

These examples use the MindCloud API key and Congress.gov connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Bills

Retrieves bills from Congress.gov.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/list-bills?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/list-bills?${params}`, {
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
      "bills": [
        {}
      ],
      "pagination": {},
      "request": {}
    }
  ],
  "meta": {}
}
```

See the full [List Bills action reference](actions/list-bills.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/congressgov/latest/actions/list-bills).
