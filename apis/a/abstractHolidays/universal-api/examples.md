# Abstract Holidays Universal API Examples

These examples use the MindCloud API key and Abstract Holidays connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Holidays

Retrieves holidays from Abstract Holidays for a country and date.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abstractHolidays/latest/actions/get-holidays?connectionId=$CONNECTION_ID&country=US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country": "US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abstractHolidays/latest/actions/get-holidays?${params}`, {
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
      "country": "string",
      "date": "string",
      "date_day": "string",
      "date_month": "string",
      "date_year": "string",
      "description": "string",
      "language": "string",
      "location": "string",
      "name": "Ava Chen",
      "name_local": "Ava Chen",
      "type": "string",
      "week_day": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Holidays action reference](actions/get-holidays.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/abstractHolidays/latest/actions/get-holidays).
