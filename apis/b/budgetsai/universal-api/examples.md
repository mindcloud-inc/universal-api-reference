# Budgets.ai Universal API Examples

These examples use the MindCloud API key and Budgets.ai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Campaigns



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/budgetsai/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&state=all" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "state": "all"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/budgetsai/latest/actions/list-campaigns?${params}`, {
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

See the full [List Campaigns action reference](actions/list-campaigns.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/budgetsai/latest/actions/list-campaigns).
