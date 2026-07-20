# College Football Data: List Pregame Win Probabilities

Retrieves pregame win probabilities from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-pregame-win-probabilities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-pregame-win-probabilities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-pregame-win-probabilities?${params}`, {
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
| `week` | number | no | Optional week filter |
| `seasonType` | string | no | Optional season type filter |
| `team` | string | no | Optional team filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "awayTeam": "string",
      "gameId": 1,
      "homeTeam": "string",
      "homeWinProbability": 1,
      "season": 1,
      "seasonType": "string",
      "spread": 1,
      "week": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `awayTeam` | string |  |
| `gameId` | number |  |
| `homeTeam` | string |  |
| `homeWinProbability` | number |  |
| `season` | number |  |
| `seasonType` | string |  |
| `spread` | number |  |
| `week` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /metrics/wp/pregame` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pregame-win-probabilities.md) for the provider-specific parameters and requirements.

