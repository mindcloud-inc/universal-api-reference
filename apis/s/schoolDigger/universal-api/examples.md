# SchoolDigger Universal API Examples

These examples use the MindCloud API key and SchoolDigger connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Autocomplete Districts

Finds district matches in SchoolDigger by partial search text.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/schoolDigger/latest/actions/autocomplete-districts?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/schoolDigger/latest/actions/autocomplete-districts?${params}`, {
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
      "city": "string",
      "districtid": "string",
      "districtName": "Ava Chen",
      "hasBoundary": true,
      "highGrade": "string",
      "latitude": 1,
      "longitude": 1,
      "lowGrade": "string",
      "rank": 1,
      "rankOf": 1,
      "rankStars": 1,
      "state": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

See the full [Autocomplete Districts action reference](actions/autocomplete-districts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/schoolDigger/latest/actions/autocomplete-districts).
