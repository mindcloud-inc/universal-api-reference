# College Football Data: List Media

Retrieves game media information from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-media?connectionId=$CONNECTION_ID&year=2025" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "year": "2025"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-media?${params}`, {
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
| `year` | number | yes | Required year filter Default: `2025`. |
| `seasonType` | string | no | Optional season type filter |
| `week` | number | no | Optional week filter |
| `team` | string | no | Optional team filter |
| `conference` | string | no | Optional conference filter |
| `mediaType` | string | no | Optional media type filter |
| `classification` | string | no | Optional division classification filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "awayConference": "string",
      "awayTeam": "string",
      "homeConference": "string",
      "homeTeam": "string",
      "id": 1,
      "isStartTimeTBD": true,
      "mediaType": "string",
      "outlet": "string",
      "season": 1,
      "seasonType": "string",
      "startTime": "string",
      "week": 1
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
| `homeConference` | string |  |
| `homeTeam` | string |  |
| `id` | number |  |
| `isStartTimeTBD` | boolean |  |
| `mediaType` | string |  |
| `outlet` | string |  |
| `season` | number |  |
| `seasonType` | string |  |
| `startTime` | string |  |
| `week` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /games/media` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-media.md) for the provider-specific parameters and requirements.

