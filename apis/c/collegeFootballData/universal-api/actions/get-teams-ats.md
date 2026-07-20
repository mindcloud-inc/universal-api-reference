# College Football Data: List Teams A T S

Retrieves team ATS summaries from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-teams-ats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-teams-ats?connectionId=$CONNECTION_ID&year=2025" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "year": "2025"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-teams-ats?${params}`, {
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
| `conference` | string | no | Optional conference filter |
| `team` | string | no | Optional team filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "atsLosses": 1,
      "atsPushes": 1,
      "atsWins": 1,
      "avgCoverMargin": 1,
      "conference": "string",
      "games": 1,
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
| `atsLosses` | number |  |
| `atsPushes` | number |  |
| `atsWins` | number |  |
| `avgCoverMargin` | number |  |
| `conference` | string |  |
| `games` | number |  |
| `team` | string |  |
| `teamId` | number |  |
| `year` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /teams/ats` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-teams-ats.md) for the provider-specific parameters and requirements.

