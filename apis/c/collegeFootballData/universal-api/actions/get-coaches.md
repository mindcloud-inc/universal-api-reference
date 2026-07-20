# College Football Data: List Coaches

Retrieves historical head coach records from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-coaches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-coaches?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-coaches?${params}`, {
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
| `firstName` | string | no | Optional first name filter |
| `lastName` | string | no | Optional last name filter |
| `team` | string | no | Optional team filter |
| `year` | number | no | Optional year filter |
| `minYear` | number | no | Optional start year range filter |
| `maxYear` | number | no | Optional end year range filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "firstName": "Ava",
      "hireDate": "string",
      "lastName": "Chen",
      "seasons": {
        "games": 1,
        "losses": 1,
        "postseasonRank": 1,
        "preseasonRank": 1,
        "school": "string",
        "spDefense": 1,
        "spOffense": 1,
        "spOverall": 1,
        "srs": 1,
        "ties": 1,
        "wins": 1,
        "year": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `firstName` | string |  |
| `hireDate` | string |  |
| `lastName` | string |  |
| `seasons.games` | number |  |
| `seasons.losses` | number |  |
| `seasons.postseasonRank` | number |  |
| `seasons.preseasonRank` | number |  |
| `seasons.school` | string |  |
| `seasons.spDefense` | number |  |
| `seasons.spOffense` | number |  |
| `seasons.spOverall` | number |  |
| `seasons.srs` | number |  |
| `seasons.ties` | number |  |
| `seasons.wins` | number |  |
| `seasons.year` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /coaches` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-coaches.md) for the provider-specific parameters and requirements.

