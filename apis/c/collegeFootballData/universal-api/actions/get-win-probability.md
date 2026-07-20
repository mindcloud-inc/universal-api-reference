# College Football Data: List Win Probability

Retrieves play win probabilities from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-win-probability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-win-probability?connectionId=$CONNECTION_ID&gameId=401756846" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "gameId": "401756846"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-win-probability?${params}`, {
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
| `gameId` | number | yes | Required game ID filter Default: `401756846`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "away": "string",
      "awayId": 1,
      "awayScore": 1,
      "distance": 1,
      "down": 1,
      "gameId": 1,
      "home": "string",
      "homeBall": true,
      "homeId": 1,
      "homeScore": 1,
      "homeWinProbability": 1,
      "playId": "string",
      "playNumber": 1,
      "playText": "string",
      "spread": 1,
      "yardLine": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `away` | string |  |
| `awayId` | number |  |
| `awayScore` | number |  |
| `distance` | number |  |
| `down` | number |  |
| `gameId` | number |  |
| `home` | string |  |
| `homeBall` | boolean |  |
| `homeId` | number |  |
| `homeScore` | number |  |
| `homeWinProbability` | number |  |
| `playId` | string |  |
| `playNumber` | number |  |
| `playText` | string |  |
| `spread` | number |  |
| `yardLine` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /metrics/wp` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-win-probability.md) for the provider-specific parameters and requirements.

