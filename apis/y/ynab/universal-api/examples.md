# YNAB Universal API Examples

These examples use the MindCloud API key and YNAB connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Plans

Retrieves plans from YNAB.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ynab/latest/actions/list-plans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ynab/latest/actions/list-plans?${params}`, {
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
      "currencyFormat": {},
      "dateFormat": {},
      "firstMonth": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "lastModifiedOn": "2026-05-07T12:00:00.000Z",
      "lastMonth": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Plans action reference](actions/list-plans.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ynab/latest/actions/list-plans).
