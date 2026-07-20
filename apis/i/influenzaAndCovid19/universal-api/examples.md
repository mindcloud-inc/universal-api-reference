# Influenza and Covid-19 Universal API Examples

These examples use the MindCloud API key and Influenza and Covid-19 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Emergency Department Visits by Demographic Category



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influenzaAndCovid19/latest/actions/list-emergency-department-visits-by-demographic-category?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/influenzaAndCovid19/latest/actions/list-emergency-department-visits-by-demographic-category?${params}`, {
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
      "demographics_type": "string",
      "demographics_values": "string",
      "geography": "string",
      "pathogen": "string",
      "percent_visits": 1,
      "week_end": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Emergency Department Visits by Demographic Category action reference](actions/list-emergency-department-visits-by-demographic-category.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/influenzaAndCovid19/latest/actions/list-emergency-department-visits-by-demographic-category).
