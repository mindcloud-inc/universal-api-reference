# College Football Data: List F P I

Retrieves historical FPI ratings from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-fpi
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-fpi?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-fpi?${params}`, {
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
| `year` | number | no | year filter, required if team not specified |
| `team` | string | no | team filter, required if year not specified |
| `conference` | string | no | Optional conference filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conference": "string",
      "efficiencies": {
        "defense": 1,
        "offense": 1,
        "overall": 1,
        "specialTeams": 1
      },
      "fpi": 1,
      "resumeRanks": {
        "averageWinProbability": 1,
        "fpi": 1,
        "gameControl": 1,
        "remainingStrengthOfSchedule": 1,
        "strengthOfRecord": 1,
        "strengthOfSchedule": 1
      },
      "team": "string",
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
| `efficiencies.defense` | number |  |
| `efficiencies.offense` | number |  |
| `efficiencies.overall` | number |  |
| `efficiencies.specialTeams` | number |  |
| `fpi` | number |  |
| `resumeRanks.averageWinProbability` | number |  |
| `resumeRanks.fpi` | number |  |
| `resumeRanks.gameControl` | number |  |
| `resumeRanks.remainingStrengthOfSchedule` | number |  |
| `resumeRanks.strengthOfRecord` | number |  |
| `resumeRanks.strengthOfSchedule` | number |  |
| `team` | string |  |
| `year` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /ratings/fpi` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fpi.md) for the provider-specific parameters and requirements.

