# College Football Data: List Rankings

Retrieves historical poll rankings from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-rankings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-rankings?connectionId=$CONNECTION_ID&year=2025" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "year": "2025"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-rankings?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "polls": {
        "poll": "string",
        "ranks": {
          "conference": "string",
          "firstPlaceVotes": 1,
          "points": 1,
          "rank": 1,
          "school": "string",
          "teamId": 1
        }
      },
      "season": 1,
      "seasonType": "string",
      "week": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `polls.poll` | string |  |
| `polls.ranks.conference` | string |  |
| `polls.ranks.firstPlaceVotes` | number |  |
| `polls.ranks.points` | number |  |
| `polls.ranks.rank` | number |  |
| `polls.ranks.school` | string |  |
| `polls.ranks.teamId` | number |  |
| `season` | number |  |
| `seasonType` | string |  |
| `week` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /rankings` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-rankings.md) for the provider-specific parameters and requirements.

