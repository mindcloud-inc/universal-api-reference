# NYC Squirrel Census: List squirrel sightings



```
GET https://connect.mindcloud.co/v1/universal/nYCSquirrelCensus/latest/actions/list-squirrel-sightings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NYC Squirrel Census `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

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

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `where` | string | no | Optional advanced SoQL predicate for the fixed NYC Squirrel Census dataset. For example: primary_fur_color = 'Gray'. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `above_ground_sighter` | string | Reported above-ground measurement when present. |
| `age` | string | Reported squirrel age when present. |
| `approaches` | boolean | Whether the squirrel approached a human. |
| `chasing` | boolean | Whether the squirrel was observed chasing. |
| `climbing` | boolean | Whether the squirrel was observed climbing. |
| `color_notes` | string | Observer fur-color notes when present. |
| `combination_of_primary_and` | string | Dataset combination of primary and highlight fur color. |
| `date` | string | Dataset sighting date representation. |
| `eating` | boolean | Whether the squirrel was observed eating. |
| `foraging` | boolean | Whether the squirrel was observed foraging. |
| `geocoded_column` | object | GeoJSON Point object for the sighting when present. |
| `hectare` | string | Central Park hectare grid identifier. |
| `hectare_squirrel_number` | string | Sighting sequence number within the session, returned as a string. |
| `highlight_fur_color` | string | Reported highlight fur color when present. |
| `indifferent` | boolean | Whether the squirrel was indifferent to humans. |
| `kuks` | boolean | Whether kuk vocalization was observed. |
| `location` | string | Initial sighting location when present. |
| `moans` | boolean | Whether moan vocalization was observed. |
| `other_activities` | string | Other observed activity notes when present. |
| `other_interactions` | string | Other squirrel-human interaction notes when present. |
| `primary_fur_color` | string | Reported primary fur color when present. |
| `quaas` | boolean | Whether quaa vocalization was observed. |
| `running` | boolean | Whether the squirrel was observed running. |
| `runs_from` | boolean | Whether the squirrel ran from humans. |
| `shift` | string | Sighting shift, such as AM or PM. |
| `specific_location` | string | Observer location notes when present. |
| `tail_flags` | boolean | Whether tail flagging was observed. |
| `tail_twitches` | boolean | Whether tail twitching was observed. |
| `unique_squirrel_id` | string | Dataset identifier for the sighting. |
| `x` | string | Longitude coordinate returned by Socrata. |
| `y` | string | Latitude coordinate returned by Socrata. |

## Native endpoint

Through the native NYC Squirrel Census API, this operation is `GET /resource/vfnx-vebw.json` (base URL `https://data.cityofnewyork.us`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-squirrel-sightings.md) for the provider-specific parameters and requirements.

