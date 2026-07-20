# College Football Data: List Adjusted Team Season Stats

Retrieves opponent-adjusted team season statistics from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-adjusted-team-season-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-adjusted-team-season-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-adjusted-team-season-stats?${params}`, {
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
| `team` | string | no | Optional team filter |
| `conference` | string | no | Optional conference filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conference": "string",
      "epa": {
        "passing": 1,
        "rushing": 1,
        "total": 1
      },
      "epaAllowed": {
        "passing": 1,
        "rushing": 1,
        "total": 1
      },
      "explosiveness": 1,
      "explosivenessAllowed": 1,
      "rushing": {
        "highlightYards": 1,
        "lineYards": 1,
        "openFieldYards": 1,
        "secondLevelYards": 1
      },
      "rushingAllowed": {
        "highlightYards": 1,
        "lineYards": 1,
        "openFieldYards": 1,
        "secondLevelYards": 1
      },
      "successRate": {
        "passingDowns": 1,
        "standardDowns": 1,
        "total": 1
      },
      "successRateAllowed": {
        "passingDowns": 1,
        "standardDowns": 1,
        "total": 1
      },
      "team": "string",
      "teamId": 1,
      "year": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conference` | string |  |
| `epa.passing` | number |  |
| `epa.rushing` | number |  |
| `epa.total` | number |  |
| `epaAllowed.passing` | number |  |
| `epaAllowed.rushing` | number |  |
| `epaAllowed.total` | number |  |
| `explosiveness` | number |  |
| `explosivenessAllowed` | number |  |
| `rushing.highlightYards` | number |  |
| `rushing.lineYards` | number |  |
| `rushing.openFieldYards` | number |  |
| `rushing.secondLevelYards` | number |  |
| `rushingAllowed.highlightYards` | number |  |
| `rushingAllowed.lineYards` | number |  |
| `rushingAllowed.openFieldYards` | number |  |
| `rushingAllowed.secondLevelYards` | number |  |
| `successRate.passingDowns` | number |  |
| `successRate.standardDowns` | number |  |
| `successRate.total` | number |  |
| `successRateAllowed.passingDowns` | number |  |
| `successRateAllowed.standardDowns` | number |  |
| `successRateAllowed.total` | number |  |
| `team` | string |  |
| `teamId` | number |  |
| `year` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /wepa/team/season` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-adjusted-team-season-stats.md) for the provider-specific parameters and requirements.

