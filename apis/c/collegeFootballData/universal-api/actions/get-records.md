# College Football Data: List Records

Retrieves historical team records from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-records?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-records?${params}`, {
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
| `year` | number | no | Year filter, required if team not specified |
| `team` | string | no | Team filter, required if year not specified |
| `conference` | string | no | Optional conference filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "awayGames": {
        "games": 1,
        "losses": 1,
        "ties": 1,
        "wins": 1
      },
      "classification": "string",
      "conference": "string",
      "conferenceGames": {
        "games": 1,
        "losses": 1,
        "ties": 1,
        "wins": 1
      },
      "division": "string",
      "expectedWins": 1,
      "homeGames": {
        "games": 1,
        "losses": 1,
        "ties": 1,
        "wins": 1
      },
      "neutralSiteGames": {
        "games": 1,
        "losses": 1,
        "ties": 1,
        "wins": 1
      },
      "postseason": {
        "games": 1,
        "losses": 1,
        "ties": 1,
        "wins": 1
      },
      "regularSeason": {
        "games": 1,
        "losses": 1,
        "ties": 1,
        "wins": 1
      },
      "team": "string",
      "teamId": 1,
      "total": {
        "games": 1,
        "losses": 1,
        "ties": 1,
        "wins": 1
      },
      "year": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `awayGames.games` | number |  |
| `awayGames.losses` | number |  |
| `awayGames.ties` | number |  |
| `awayGames.wins` | number |  |
| `classification` | string |  |
| `conference` | string |  |
| `conferenceGames.games` | number |  |
| `conferenceGames.losses` | number |  |
| `conferenceGames.ties` | number |  |
| `conferenceGames.wins` | number |  |
| `division` | string |  |
| `expectedWins` | number |  |
| `homeGames.games` | number |  |
| `homeGames.losses` | number |  |
| `homeGames.ties` | number |  |
| `homeGames.wins` | number |  |
| `neutralSiteGames.games` | number |  |
| `neutralSiteGames.losses` | number |  |
| `neutralSiteGames.ties` | number |  |
| `neutralSiteGames.wins` | number |  |
| `postseason.games` | number |  |
| `postseason.losses` | number |  |
| `postseason.ties` | number |  |
| `postseason.wins` | number |  |
| `regularSeason.games` | number |  |
| `regularSeason.losses` | number |  |
| `regularSeason.ties` | number |  |
| `regularSeason.wins` | number |  |
| `team` | string |  |
| `teamId` | number |  |
| `total.games` | number |  |
| `total.losses` | number |  |
| `total.ties` | number |  |
| `total.wins` | number |  |
| `year` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /records` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-records.md) for the provider-specific parameters and requirements.

