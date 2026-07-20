# Jobicy Universal API Examples

These examples use the MindCloud API key and Jobicy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Accounting and Finance Remote Jobs



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jobicy/latest/actions/list-accounting-and-finance-remote-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jobicy/latest/actions/list-accounting-and-finance-remote-jobs?${params}`, {
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

See the full [List Accounting and Finance Remote Jobs action reference](actions/list-accounting-and-finance-remote-jobs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jobicy/latest/actions/list-accounting-and-finance-remote-jobs).
