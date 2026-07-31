# NYC Squirrel Census Universal API Examples

These examples use the MindCloud API key and NYC Squirrel Census connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List squirrel sightings



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nYCSquirrelCensus/latest/actions/list-squirrel-sightings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nYCSquirrelCensus/latest/actions/list-squirrel-sightings?${params}`, {
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
      "above_ground_sighter": "string",
      "age": "string",
      "approaches": true,
      "chasing": true,
      "climbing": true,
      "color_notes": "string",
      "combination_of_primary_and": "string",
      "date": "string",
      "eating": true,
      "foraging": true,
      "geocoded_column": {},
      "hectare": "string",
      "hectare_squirrel_number": "string",
      "highlight_fur_color": "string",
      "indifferent": true,
      "kuks": true,
      "location": "string",
      "moans": true,
      "other_activities": "string",
      "other_interactions": "string",
      "primary_fur_color": "string",
      "quaas": true,
      "running": true,
      "runs_from": true,
      "shift": "string",
      "specific_location": "string",
      "tail_flags": true,
      "tail_twitches": true,
      "unique_squirrel_id": "string",
      "x": "string",
      "y": "string"
    }
  ],
  "meta": {}
}
```

See the full [List squirrel sightings action reference](actions/list-squirrel-sightings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nYCSquirrelCensus/latest/actions/list-squirrel-sightings).
