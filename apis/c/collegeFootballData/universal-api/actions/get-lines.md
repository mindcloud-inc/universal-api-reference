# College Football Data: List Lines

Retrieves historical betting lines from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-lines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-lines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-lines?${params}`, {
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
| `gameId` | number | no | Optional gameId filter |
| `year` | number | no | Year filter, required if game id not specified |
| `seasonType` | string | no | Optional season type filter |
| `week` | number | no | Optional week filter |
| `team` | string | no | Optional team filter |
| `home` | string | no | Optional home team filter |
| `away` | string | no | Optional away team filter |
| `conference` | string | no | Optional conference filter |
| `provider` | string | no | Optional provider name filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "awayClassification": "string",
      "awayConference": "string",
      "awayScore": 1,
      "awayTeam": "string",
      "awayTeamId": 1,
      "homeClassification": "string",
      "homeConference": "string",
      "homeScore": 1,
      "homeTeam": "string",
      "homeTeamId": 1,
      "id": 1,
      "lines": {
        "awayMoneyline": 1,
        "formattedSpread": "string",
        "homeMoneyline": 1,
        "overUnder": 1,
        "overUnderOpen": 1,
        "provider": "string",
        "spread": 1,
        "spreadOpen": 1
      },
      "season": 1,
      "seasonType": "string",
      "startDate": "string",
      "week": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `awayClassification` | string |  |
| `awayConference` | string |  |
| `awayScore` | number |  |
| `awayTeam` | string |  |
| `awayTeamId` | number |  |
| `homeClassification` | string |  |
| `homeConference` | string |  |
| `homeScore` | number |  |
| `homeTeam` | string |  |
| `homeTeamId` | number |  |
| `id` | number |  |
| `lines.awayMoneyline` | number |  |
| `lines.formattedSpread` | string |  |
| `lines.homeMoneyline` | number |  |
| `lines.overUnder` | number |  |
| `lines.overUnderOpen` | number |  |
| `lines.provider` | string |  |
| `lines.spread` | number |  |
| `lines.spreadOpen` | number |  |
| `season` | number |  |
| `seasonType` | string |  |
| `startDate` | string |  |
| `week` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /lines` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lines.md) for the provider-specific parameters and requirements.

