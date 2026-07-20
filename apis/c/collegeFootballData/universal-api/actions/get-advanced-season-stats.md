# College Football Data: List Advanced Season Stats

Retrieves advanced team season statistics from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-advanced-season-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-advanced-season-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-advanced-season-stats?${params}`, {
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
| `excludeGarbageTime` | boolean | no | Garbage time exclusion filter, defaults to false |
| `startWeek` | number | no | Optional start week range filter |
| `endWeek` | number | no | Optional end week range filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conference": "string",
      "defense": {
        "drives": 1,
        "explosiveness": 1,
        "fieldPosition": {
          "averagePredictedPoints": 1,
          "averageStart": 1
        },
        "havoc": {
          "db": 1,
          "frontSeven": 1,
          "total": 1
        },
        "lineYards": 1,
        "lineYardsTotal": 1,
        "openFieldYards": 1,
        "openFieldYardsTotal": 1,
        "passingDowns": {
          "explosiveness": 1,
          "ppa": 1,
          "rate": 1,
          "successRate": 1,
          "totalPPA": 1
        },
        "passingPlays": {
          "explosiveness": 1,
          "ppa": 1,
          "rate": 1,
          "successRate": 1,
          "totalPPA": 1
        },
        "plays": 1,
        "pointsPerOpportunity": 1,
        "powerSuccess": 1,
        "ppa": 1,
        "rushingPlays": {
          "explosiveness": 1,
          "ppa": 1,
          "rate": 1,
          "successRate": 1,
          "totalPPA": 1
        },
        "secondLevelYards": 1,
        "secondLevelYardsTotal": 1,
        "standardDowns": {
          "explosiveness": 1,
          "ppa": 1,
          "rate": 1,
          "successRate": 1
        },
        "stuffRate": 1,
        "successRate": 1,
        "totalOpportunies": 1,
        "totalPPA": 1
      },
      "offense": {
        "drives": 1,
        "explosiveness": 1,
        "fieldPosition": {
          "averagePredictedPoints": 1,
          "averageStart": 1
        },
        "havoc": {
          "db": 1,
          "frontSeven": 1,
          "total": 1
        },
        "lineYards": 1,
        "lineYardsTotal": 1,
        "openFieldYards": 1,
        "openFieldYardsTotal": 1,
        "passingDowns": {
          "explosiveness": 1,
          "ppa": 1,
          "rate": 1,
          "successRate": 1
        },
        "passingPlays": {
          "explosiveness": 1,
          "ppa": 1,
          "rate": 1,
          "successRate": 1,
          "totalPPA": 1
        },
        "plays": 1,
        "pointsPerOpportunity": 1,
        "powerSuccess": 1,
        "ppa": 1,
        "rushingPlays": {
          "explosiveness": 1,
          "ppa": 1,
          "rate": 1,
          "successRate": 1,
          "totalPPA": 1
        },
        "secondLevelYards": 1,
        "secondLevelYardsTotal": 1,
        "standardDowns": {
          "explosiveness": 1,
          "ppa": 1,
          "rate": 1,
          "successRate": 1
        },
        "stuffRate": 1,
        "successRate": 1,
        "totalOpportunies": 1,
        "totalPPA": 1
      },
      "season": 1,
      "team": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conference` | string |  |
| `defense.drives` | number |  |
| `defense.explosiveness` | number |  |
| `defense.fieldPosition.averagePredictedPoints` | number |  |
| `defense.fieldPosition.averageStart` | number |  |
| `defense.havoc.db` | number |  |
| `defense.havoc.frontSeven` | number |  |
| `defense.havoc.total` | number |  |
| `defense.lineYards` | number |  |
| `defense.lineYardsTotal` | number |  |
| `defense.openFieldYards` | number |  |
| `defense.openFieldYardsTotal` | number |  |
| `defense.passingDowns.explosiveness` | number |  |
| `defense.passingDowns.ppa` | number |  |
| `defense.passingDowns.rate` | number |  |
| `defense.passingDowns.successRate` | number |  |
| `defense.passingDowns.totalPPA` | number |  |
| `defense.passingPlays.explosiveness` | number |  |
| `defense.passingPlays.ppa` | number |  |
| `defense.passingPlays.rate` | number |  |
| `defense.passingPlays.successRate` | number |  |
| `defense.passingPlays.totalPPA` | number |  |
| `defense.plays` | number |  |
| `defense.pointsPerOpportunity` | number |  |
| `defense.powerSuccess` | number |  |
| `defense.ppa` | number |  |
| `defense.rushingPlays.explosiveness` | number |  |
| `defense.rushingPlays.ppa` | number |  |
| `defense.rushingPlays.rate` | number |  |
| `defense.rushingPlays.successRate` | number |  |
| `defense.rushingPlays.totalPPA` | number |  |
| `defense.secondLevelYards` | number |  |
| `defense.secondLevelYardsTotal` | number |  |
| `defense.standardDowns.explosiveness` | number |  |
| `defense.standardDowns.ppa` | number |  |
| `defense.standardDowns.rate` | number |  |
| `defense.standardDowns.successRate` | number |  |
| `defense.stuffRate` | number |  |
| `defense.successRate` | number |  |
| `defense.totalOpportunies` | number |  |
| `defense.totalPPA` | number |  |
| `offense.drives` | number |  |
| `offense.explosiveness` | number |  |
| `offense.fieldPosition.averagePredictedPoints` | number |  |
| `offense.fieldPosition.averageStart` | number |  |
| `offense.havoc.db` | number |  |
| `offense.havoc.frontSeven` | number |  |
| `offense.havoc.total` | number |  |
| `offense.lineYards` | number |  |
| `offense.lineYardsTotal` | number |  |
| `offense.openFieldYards` | number |  |
| `offense.openFieldYardsTotal` | number |  |
| `offense.passingDowns.explosiveness` | number |  |
| `offense.passingDowns.ppa` | number |  |
| `offense.passingDowns.rate` | number |  |
| `offense.passingDowns.successRate` | number |  |
| `offense.passingPlays.explosiveness` | number |  |
| `offense.passingPlays.ppa` | number |  |
| `offense.passingPlays.rate` | number |  |
| `offense.passingPlays.successRate` | number |  |
| `offense.passingPlays.totalPPA` | number |  |
| `offense.plays` | number |  |
| `offense.pointsPerOpportunity` | number |  |
| `offense.powerSuccess` | number |  |
| `offense.ppa` | number |  |
| `offense.rushingPlays.explosiveness` | number |  |
| `offense.rushingPlays.ppa` | number |  |
| `offense.rushingPlays.rate` | number |  |
| `offense.rushingPlays.successRate` | number |  |
| `offense.rushingPlays.totalPPA` | number |  |
| `offense.secondLevelYards` | number |  |
| `offense.secondLevelYardsTotal` | number |  |
| `offense.standardDowns.explosiveness` | number |  |
| `offense.standardDowns.ppa` | number |  |
| `offense.standardDowns.rate` | number |  |
| `offense.standardDowns.successRate` | number |  |
| `offense.stuffRate` | number |  |
| `offense.successRate` | number |  |
| `offense.totalOpportunies` | number |  |
| `offense.totalPPA` | number |  |
| `season` | number |  |
| `team` | string |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /stats/season/advanced` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-advanced-season-stats.md) for the provider-specific parameters and requirements.

