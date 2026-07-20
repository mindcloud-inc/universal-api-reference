# Merge Universal API Examples

These examples use the MindCloud API key and Merge connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List HRIS Linked Accounts



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/merge/latest/actions/list-hris-linked-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/merge/latest/actions/list-hris-linked-accounts?${params}`, {
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
      "next": {},
      "previous": {},
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List HRIS Linked Accounts action reference](actions/list-hris-linked-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/merge/latest/actions/list-hris-linked-accounts).
