# Calculate Working Day Universal API Examples

These examples use the MindCloud API key and Calculate Working Day connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Basic Next Working Day

Retrieves the next Monday-to-Friday working day.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calculateWorkingDay/latest/actions/basic-next-working-day?connectionId=$CONNECTION_ID&date=2026-04-29" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "2026-04-29"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calculateWorkingDay/latest/actions/basic-next-working-day?${params}`, {
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
      "input_date": "string",
      "message_from_developer": "string",
      "more_info": "string",
      "next_working_day": "string"
    }
  ],
  "meta": {}
}
```

See the full [Basic Next Working Day action reference](actions/basic-next-working-day.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/calculateWorkingDay/latest/actions/basic-next-working-day).
