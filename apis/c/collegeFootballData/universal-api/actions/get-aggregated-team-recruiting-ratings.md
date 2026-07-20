# College Football Data: List Aggregated Team Recruiting Ratings

Retrieves aggregated team recruiting ratings from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-aggregated-team-recruiting-ratings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-aggregated-team-recruiting-ratings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-aggregated-team-recruiting-ratings?${params}`, {
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
| `team` | string | no | Optional team filter |
| `conference` | string | no | Optional conference filter |
| `recruitType` | string | no | Optional recruit type filter, defaults to HighSchool |
| `startYear` | number | no | Optional start year range, defaults to 2000 |
| `endYear` | number | no | Optional end year range, defaults to current year |

## Response

```json
{
  "success": true,
  "data": [
    {
      "averageRating": 1,
      "averageStars": 1,
      "commits": 1,
      "conference": "string",
      "positionGroup": "string",
      "team": "string",
      "totalRating": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `averageRating` | number |  |
| `averageStars` | number |  |
| `commits` | number |  |
| `conference` | string |  |
| `positionGroup` | string |  |
| `team` | string |  |
| `totalRating` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /recruiting/groups` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-aggregated-team-recruiting-ratings.md) for the provider-specific parameters and requirements.

