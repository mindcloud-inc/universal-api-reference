# Strategypoint Universal API Examples

These examples use the MindCloud API key and Strategypoint connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Scorecards

Retrieves scorecards from Strategypoint.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-scorecards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-scorecards?${params}`, {
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
      "active": true,
      "archived": true,
      "favorite": true,
      "name": "Ava Chen",
      "ownerId": 1,
      "periodId": 1,
      "scorecardId": 1,
      "vision": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Scorecards action reference](actions/list-scorecards.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/strategypoint/latest/actions/list-scorecards).
