# College Football Data: List Predicted Points Added By Team

Retrieves team PPA metrics by season from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-predicted-points-added-by-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-predicted-points-added-by-team?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-predicted-points-added-by-team?${params}`, {
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
| `conference` | string | no | Conference abbreviation filter |
| `excludeGarbageTime` | boolean | no | Exclude garbage time plays |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conference": "string",
      "defense": {
        "cumulative": {
          "passing": 1,
          "rushing": 1,
          "total": 1
        },
        "firstDown": 1,
        "overall": 1,
        "passing": 1,
        "rushing": 1,
        "secondDown": 1,
        "thirdDown": 1
      },
      "offense": {
        "cumulative": {
          "passing": 1,
          "rushing": 1,
          "total": 1
        },
        "firstDown": 1,
        "overall": 1,
        "passing": 1,
        "rushing": 1,
        "secondDown": 1,
        "thirdDown": 1
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
| `defense.cumulative.passing` | number |  |
| `defense.cumulative.rushing` | number |  |
| `defense.cumulative.total` | number |  |
| `defense.firstDown` | number |  |
| `defense.overall` | number |  |
| `defense.passing` | number |  |
| `defense.rushing` | number |  |
| `defense.secondDown` | number |  |
| `defense.thirdDown` | number |  |
| `offense.cumulative.passing` | number |  |
| `offense.cumulative.rushing` | number |  |
| `offense.cumulative.total` | number |  |
| `offense.firstDown` | number |  |
| `offense.overall` | number |  |
| `offense.passing` | number |  |
| `offense.rushing` | number |  |
| `offense.secondDown` | number |  |
| `offense.thirdDown` | number |  |
| `season` | number |  |
| `team` | string |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /ppa/teams` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-predicted-points-added-by-team.md) for the provider-specific parameters and requirements.

