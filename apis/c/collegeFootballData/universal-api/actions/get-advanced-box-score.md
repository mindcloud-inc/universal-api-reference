# College Football Data: Get Advanced Box Score

Retrieves an advanced box score from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-advanced-box-score
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-advanced-box-score?connectionId=$CONNECTION_ID&id=401756846" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "401756846"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-advanced-box-score?${params}`, {
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
| `id` | number | yes | Required game id filter Default: `401756846`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "gameInfo": {
        "awayPoints": 1,
        "awayTeam": "string",
        "awayWinProb": 1,
        "excitement": 1,
        "homePoints": 1,
        "homeTeam": "string",
        "homeWinner": true,
        "homeWinProb": 1
      },
      "players": {
        "ppa": {
          "average": {
            "passing": 1,
            "quarter1": 1,
            "quarter2": 1,
            "quarter3": 1,
            "quarter4": 1,
            "rushing": 1,
            "total": 1
          },
          "cumulative": {
            "passing": 1,
            "quarter1": 1,
            "quarter2": 1,
            "quarter3": 1,
            "quarter4": 1,
            "rushing": 1,
            "total": 1
          },
          "player": "string",
          "position": "string",
          "team": "string"
        },
        "usage": {
          "passing": 1,
          "player": "string",
          "position": "string",
          "quarter1": 1,
          "quarter2": 1,
          "quarter3": 1,
          "quarter4": 1,
          "rushing": 1,
          "team": "string",
          "total": 1
        }
      },
      "teams": {
        "cumulativePpa": {
          "overall": {
            "quarter1": 1,
            "quarter2": 1,
            "quarter3": 1,
            "quarter4": 1,
            "total": 1
          },
          "passing": {
            "quarter1": 1,
            "quarter2": 1,
            "quarter3": 1,
            "quarter4": 1,
            "total": 1
          },
          "plays": 1,
          "rushing": {
            "quarter1": 1,
            "quarter2": 1,
            "quarter3": 1,
            "quarter4": 1,
            "total": 1
          },
          "team": "string"
        },
        "explosiveness": {
          "overall": {
            "quarter1": 1,
            "quarter2": 1,
            "quarter3": 1,
            "quarter4": 1,
            "total": 1
          },
          "team": "string"
        },
        "fieldPosition": {
          "averageStart": 1,
          "averageStartingPredictedPoints": 1,
          "team": "string"
        },
        "havoc": {
          "db": 1,
          "frontSeven": 1,
          "team": "string",
          "total": 1
        },
        "ppa": {
          "overall": {
            "quarter1": 1,
            "quarter2": 1,
            "quarter3": 1,
            "quarter4": 1,
            "total": 1
          },
          "passing": {
            "quarter1": 1,
            "quarter2": 1,
            "quarter3": 1,
            "quarter4": 1,
            "total": 1
          },
          "plays": 1,
          "rushing": {
            "quarter1": 1,
            "quarter2": 1,
            "quarter3": 1,
            "quarter4": 1,
            "total": 1
          },
          "team": "string"
        },
        "rushing": {
          "lineYards": 1,
          "lineYardsAverage": 1,
          "openFieldYards": 1,
          "openFieldYardsAverage": 1,
          "powerSuccess": 1,
          "secondLevelYards": 1,
          "secondLevelYardsAverage": 1,
          "stuffRate": 1,
          "team": "string"
        },
        "scoringOpportunities": {
          "opportunities": 1,
          "points": 1,
          "pointsPerOpportunity": 1,
          "team": "string"
        },
        "successRates": {
          "overall": {
            "quarter1": 1,
            "quarter2": 1,
            "quarter3": 1,
            "quarter4": 1,
            "total": 1
          },
          "passingDowns": {
            "quarter1": 1,
            "quarter2": 1,
            "quarter3": 1,
            "quarter4": 1,
            "total": 1
          },
          "standardDowns": {
            "quarter1": 1,
            "quarter2": 1,
            "quarter3": 1,
            "quarter4": 1,
            "total": 1
          },
          "team": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gameInfo.awayPoints` | number |  |
| `gameInfo.awayTeam` | string |  |
| `gameInfo.awayWinProb` | number |  |
| `gameInfo.excitement` | number |  |
| `gameInfo.homePoints` | number |  |
| `gameInfo.homeTeam` | string |  |
| `gameInfo.homeWinner` | boolean |  |
| `gameInfo.homeWinProb` | number |  |
| `players.ppa.average.passing` | number |  |
| `players.ppa.average.quarter1` | number |  |
| `players.ppa.average.quarter2` | number |  |
| `players.ppa.average.quarter3` | number |  |
| `players.ppa.average.quarter4` | number |  |
| `players.ppa.average.rushing` | number |  |
| `players.ppa.average.total` | number |  |
| `players.ppa.cumulative.passing` | number |  |
| `players.ppa.cumulative.quarter1` | number |  |
| `players.ppa.cumulative.quarter2` | number |  |
| `players.ppa.cumulative.quarter3` | number |  |
| `players.ppa.cumulative.quarter4` | number |  |
| `players.ppa.cumulative.rushing` | number |  |
| `players.ppa.cumulative.total` | number |  |
| `players.ppa.player` | string |  |
| `players.ppa.position` | string |  |
| `players.ppa.team` | string |  |
| `players.usage.passing` | number |  |
| `players.usage.player` | string |  |
| `players.usage.position` | string |  |
| `players.usage.quarter1` | number |  |
| `players.usage.quarter2` | number |  |
| `players.usage.quarter3` | number |  |
| `players.usage.quarter4` | number |  |
| `players.usage.rushing` | number |  |
| `players.usage.team` | string |  |
| `players.usage.total` | number |  |
| `teams.cumulativePpa.overall.quarter1` | number |  |
| `teams.cumulativePpa.overall.quarter2` | number |  |
| `teams.cumulativePpa.overall.quarter3` | number |  |
| `teams.cumulativePpa.overall.quarter4` | number |  |
| `teams.cumulativePpa.overall.total` | number |  |
| `teams.cumulativePpa.passing.quarter1` | number |  |
| `teams.cumulativePpa.passing.quarter2` | number |  |
| `teams.cumulativePpa.passing.quarter3` | number |  |
| `teams.cumulativePpa.passing.quarter4` | number |  |
| `teams.cumulativePpa.passing.total` | number |  |
| `teams.cumulativePpa.plays` | number |  |
| `teams.cumulativePpa.rushing.quarter1` | number |  |
| `teams.cumulativePpa.rushing.quarter2` | number |  |
| `teams.cumulativePpa.rushing.quarter3` | number |  |
| `teams.cumulativePpa.rushing.quarter4` | number |  |
| `teams.cumulativePpa.rushing.total` | number |  |
| `teams.cumulativePpa.team` | string |  |
| `teams.explosiveness.overall.quarter1` | number |  |
| `teams.explosiveness.overall.quarter2` | number |  |
| `teams.explosiveness.overall.quarter3` | number |  |
| `teams.explosiveness.overall.quarter4` | number |  |
| `teams.explosiveness.overall.total` | number |  |
| `teams.explosiveness.team` | string |  |
| `teams.fieldPosition.averageStart` | number |  |
| `teams.fieldPosition.averageStartingPredictedPoints` | number |  |
| `teams.fieldPosition.team` | string |  |
| `teams.havoc.db` | number |  |
| `teams.havoc.frontSeven` | number |  |
| `teams.havoc.team` | string |  |
| `teams.havoc.total` | number |  |
| `teams.ppa.overall.quarter1` | number |  |
| `teams.ppa.overall.quarter2` | number |  |
| `teams.ppa.overall.quarter3` | number |  |
| `teams.ppa.overall.quarter4` | number |  |
| `teams.ppa.overall.total` | number |  |
| `teams.ppa.passing.quarter1` | number |  |
| `teams.ppa.passing.quarter2` | number |  |
| `teams.ppa.passing.quarter3` | number |  |
| `teams.ppa.passing.quarter4` | number |  |
| `teams.ppa.passing.total` | number |  |
| `teams.ppa.plays` | number |  |
| `teams.ppa.rushing.quarter1` | number |  |
| `teams.ppa.rushing.quarter2` | number |  |
| `teams.ppa.rushing.quarter3` | number |  |
| `teams.ppa.rushing.quarter4` | number |  |
| `teams.ppa.rushing.total` | number |  |
| `teams.ppa.team` | string |  |
| `teams.rushing.lineYards` | number |  |
| `teams.rushing.lineYardsAverage` | number |  |
| `teams.rushing.openFieldYards` | number |  |
| `teams.rushing.openFieldYardsAverage` | number |  |
| `teams.rushing.powerSuccess` | number |  |
| `teams.rushing.secondLevelYards` | number |  |
| `teams.rushing.secondLevelYardsAverage` | number |  |
| `teams.rushing.stuffRate` | number |  |
| `teams.rushing.team` | string |  |
| `teams.scoringOpportunities.opportunities` | number |  |
| `teams.scoringOpportunities.points` | number |  |
| `teams.scoringOpportunities.pointsPerOpportunity` | number |  |
| `teams.scoringOpportunities.team` | string |  |
| `teams.successRates.overall.quarter1` | number |  |
| `teams.successRates.overall.quarter2` | number |  |
| `teams.successRates.overall.quarter3` | number |  |
| `teams.successRates.overall.quarter4` | number |  |
| `teams.successRates.overall.total` | number |  |
| `teams.successRates.passingDowns.quarter1` | number |  |
| `teams.successRates.passingDowns.quarter2` | number |  |
| `teams.successRates.passingDowns.quarter3` | number |  |
| `teams.successRates.passingDowns.quarter4` | number |  |
| `teams.successRates.passingDowns.total` | number |  |
| `teams.successRates.standardDowns.quarter1` | number |  |
| `teams.successRates.standardDowns.quarter2` | number |  |
| `teams.successRates.standardDowns.quarter3` | number |  |
| `teams.successRates.standardDowns.quarter4` | number |  |
| `teams.successRates.standardDowns.total` | number |  |
| `teams.successRates.team` | string |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /game/box/advanced` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-advanced-box-score.md) for the provider-specific parameters and requirements.

