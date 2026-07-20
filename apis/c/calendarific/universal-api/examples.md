# Calendarific Universal API Examples

These examples use the MindCloud API key and Calendarific connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Countries

Retrieves supported countries from Calendarific.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendarific/latest/actions/list-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calendarific/latest/actions/list-countries?${params}`, {
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
      "countryName": "Ava Chen",
      "flagUnicode": "string",
      "iso3166": "string",
      "supportedLanguages": 1,
      "totalHolidays": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Countries action reference](actions/list-countries.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/calendarific/latest/actions/list-countries).
