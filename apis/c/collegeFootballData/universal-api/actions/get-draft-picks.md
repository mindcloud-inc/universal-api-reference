# College Football Data: List Draft Picks

Retrieves historical NFL draft picks from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-draft-picks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-draft-picks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-draft-picks?${params}`, {
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
| `year` | number | no | Optional year filter |
| `team` | string | no | Optional NFL team filter |
| `school` | string | no | Optional college team filter |
| `conference` | string | no | Optional college conference filter |
| `position` | string | no | Optional position classification filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collegeAthleteId": 1,
      "collegeConference": "string",
      "collegeId": 1,
      "collegeTeam": "string",
      "height": 1,
      "hometownInfo": {
        "city": "string",
        "country": "string",
        "countyFips": "string",
        "latitude": "string",
        "longitude": "string",
        "state": "string"
      },
      "name": "Ava Chen",
      "nflAthleteId": 1,
      "nflTeam": "string",
      "nflTeamId": 1,
      "overall": 1,
      "pick": 1,
      "position": "string",
      "preDraftGrade": 1,
      "preDraftPositionRanking": 1,
      "preDraftRanking": 1,
      "round": 1,
      "weight": 1,
      "year": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collegeAthleteId` | number |  |
| `collegeConference` | string |  |
| `collegeId` | number |  |
| `collegeTeam` | string |  |
| `height` | number |  |
| `hometownInfo.city` | string |  |
| `hometownInfo.country` | string |  |
| `hometownInfo.countyFips` | string |  |
| `hometownInfo.latitude` | string |  |
| `hometownInfo.longitude` | string |  |
| `hometownInfo.state` | string |  |
| `name` | string |  |
| `nflAthleteId` | number |  |
| `nflTeam` | string |  |
| `nflTeamId` | number |  |
| `overall` | number |  |
| `pick` | number |  |
| `position` | string |  |
| `preDraftGrade` | number |  |
| `preDraftPositionRanking` | number |  |
| `preDraftRanking` | number |  |
| `round` | number |  |
| `weight` | number |  |
| `year` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /draft/picks` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-draft-picks.md) for the provider-specific parameters and requirements.

