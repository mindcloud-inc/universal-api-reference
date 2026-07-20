# Major League Baseball Universal API Examples

These examples use the MindCloud API key and Major League Baseball connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get attendance



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/majorLeagueBaseball/latest/actions/attendance-attendance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/majorLeagueBaseball/latest/actions/attendance-attendance?${params}`, {
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
      "date": "string",
      "leagueId": "string",
      "season": "string",
      "teamId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get attendance action reference](actions/attendance-attendance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/majorLeagueBaseball/latest/actions/attendance-attendance).
