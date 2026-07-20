# College Football Data: List Weather

Retrieves game weather data from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-weather
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-weather?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-weather?${params}`, {
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
| `year` | number | no | Year filter, required if game id not specified |
| `seasonType` | string | no | Optional season type filter |
| `week` | number | no | Optional week filter |
| `team` | string | no | Optional team filter |
| `conference` | string | no | Optional conference filter |
| `classification` | string | no | Optional division classification filter |
| `gameId` | number | no | Filter for retrieving a single game |

## Response

```json
{
  "success": true,
  "data": [
    {
      "awayConference": "string",
      "awayTeam": "string",
      "dewPoint": 1,
      "gameIndoors": true,
      "homeConference": "string",
      "homeTeam": "string",
      "humidity": 1,
      "id": 1,
      "precipitation": 1,
      "pressure": 1,
      "season": 1,
      "seasonType": "string",
      "snowfall": 1,
      "startTime": "string",
      "temperature": 1,
      "venue": "string",
      "venueId": 1,
      "weatherCondition": "string",
      "weatherConditionCode": 1,
      "week": 1,
      "windDirection": 1,
      "windSpeed": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `awayConference` | string |  |
| `awayTeam` | string |  |
| `dewPoint` | number |  |
| `gameIndoors` | boolean |  |
| `homeConference` | string |  |
| `homeTeam` | string |  |
| `humidity` | number |  |
| `id` | number |  |
| `precipitation` | number |  |
| `pressure` | number |  |
| `season` | number |  |
| `seasonType` | string |  |
| `snowfall` | number |  |
| `startTime` | string |  |
| `temperature` | number |  |
| `venue` | string |  |
| `venueId` | number |  |
| `weatherCondition` | string |  |
| `weatherConditionCode` | number |  |
| `week` | number |  |
| `windDirection` | number |  |
| `windSpeed` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /games/weather` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-weather.md) for the provider-specific parameters and requirements.

