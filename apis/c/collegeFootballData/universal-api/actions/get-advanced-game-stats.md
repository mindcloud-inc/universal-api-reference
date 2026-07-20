# College Football Data: List Advanced Game Stats

Retrieves advanced game statistics from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-advanced-game-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-advanced-game-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-advanced-game-stats?${params}`, {
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
| `week` | number | no | Optional week filter |
| `opponent` | string | no | Optional opponent filter |
| `excludeGarbageTime` | boolean | no | Garbage time exclusion filter, defaults to false |
| `seasonType` | string | no | Optional season type filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "defense": {
        "drives": 1,
        "explosiveness": 1,
        "lineYards": 1,
        "lineYardsTotal": 1,
        "openFieldYards": 1,
        "openFieldYardsTotal": 1,
        "passingDowns": {
          "explosiveness": 1,
          "ppa": 1,
          "successRate": 1
        },
        "passingPlays": {
          "explosiveness": 1,
          "ppa": 1,
          "successRate": 1,
          "totalPPA": 1
        },
        "plays": 1,
        "powerSuccess": 1,
        "ppa": 1,
        "rushingPlays": {
          "explosiveness": 1,
          "ppa": 1,
          "successRate": 1,
          "totalPPA": 1
        },
        "secondLevelYards": 1,
        "secondLevelYardsTotal": 1,
        "standardDowns": {
          "explosiveness": 1,
          "ppa": 1,
          "successRate": 1
        },
        "stuffRate": 1,
        "successRate": 1,
        "totalPPA": 1
      },
      "gameId": 1,
      "offense": {
        "drives": 1,
        "explosiveness": 1,
        "lineYards": 1,
        "lineYardsTotal": 1,
        "openFieldYards": 1,
        "openFieldYardsTotal": 1,
        "passingDowns": {
          "explosiveness": 1,
          "ppa": 1,
          "successRate": 1
        },
        "passingPlays": {
          "explosiveness": 1,
          "ppa": 1,
          "successRate": 1,
          "totalPPA": 1
        },
        "plays": 1,
        "powerSuccess": 1,
        "ppa": 1,
        "rushingPlays": {
          "explosiveness": 1,
          "ppa": 1,
          "successRate": 1,
          "totalPPA": 1
        },
        "secondLevelYards": 1,
        "secondLevelYardsTotal": 1,
        "standardDowns": {
          "explosiveness": 1,
          "ppa": 1,
          "successRate": 1
        },
        "stuffRate": 1,
        "successRate": 1,
        "totalPPA": 1
      },
      "opponent": "string",
      "season": 1,
      "seasonType": "string",
      "team": "string",
      "week": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defense.drives` | number |  |
| `defense.explosiveness` | number |  |
| `defense.lineYards` | number |  |
| `defense.lineYardsTotal` | number |  |
| `defense.openFieldYards` | number |  |
| `defense.openFieldYardsTotal` | number |  |
| `defense.passingDowns.explosiveness` | number |  |
| `defense.passingDowns.ppa` | number |  |
| `defense.passingDowns.successRate` | number |  |
| `defense.passingPlays.explosiveness` | number |  |
| `defense.passingPlays.ppa` | number |  |
| `defense.passingPlays.successRate` | number |  |
| `defense.passingPlays.totalPPA` | number |  |
| `defense.plays` | number |  |
| `defense.powerSuccess` | number |  |
| `defense.ppa` | number |  |
| `defense.rushingPlays.explosiveness` | number |  |
| `defense.rushingPlays.ppa` | number |  |
| `defense.rushingPlays.successRate` | number |  |
| `defense.rushingPlays.totalPPA` | number |  |
| `defense.secondLevelYards` | number |  |
| `defense.secondLevelYardsTotal` | number |  |
| `defense.standardDowns.explosiveness` | number |  |
| `defense.standardDowns.ppa` | number |  |
| `defense.standardDowns.successRate` | number |  |
| `defense.stuffRate` | number |  |
| `defense.successRate` | number |  |
| `defense.totalPPA` | number |  |
| `gameId` | number |  |
| `offense.drives` | number |  |
| `offense.explosiveness` | number |  |
| `offense.lineYards` | number |  |
| `offense.lineYardsTotal` | number |  |
| `offense.openFieldYards` | number |  |
| `offense.openFieldYardsTotal` | number |  |
| `offense.passingDowns.explosiveness` | number |  |
| `offense.passingDowns.ppa` | number |  |
| `offense.passingDowns.successRate` | number |  |
| `offense.passingPlays.explosiveness` | number |  |
| `offense.passingPlays.ppa` | number |  |
| `offense.passingPlays.successRate` | number |  |
| `offense.passingPlays.totalPPA` | number |  |
| `offense.plays` | number |  |
| `offense.powerSuccess` | number |  |
| `offense.ppa` | number |  |
| `offense.rushingPlays.explosiveness` | number |  |
| `offense.rushingPlays.ppa` | number |  |
| `offense.rushingPlays.successRate` | number |  |
| `offense.rushingPlays.totalPPA` | number |  |
| `offense.secondLevelYards` | number |  |
| `offense.secondLevelYardsTotal` | number |  |
| `offense.standardDowns.explosiveness` | number |  |
| `offense.standardDowns.ppa` | number |  |
| `offense.standardDowns.successRate` | number |  |
| `offense.stuffRate` | number |  |
| `offense.successRate` | number |  |
| `offense.totalPPA` | number |  |
| `opponent` | string |  |
| `season` | number |  |
| `seasonType` | string |  |
| `team` | string |  |
| `week` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /stats/game/advanced` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-advanced-game-stats.md) for the provider-specific parameters and requirements.

