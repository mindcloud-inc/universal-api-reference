# College Football Data: List Conference S P

Retrieves conference SP+ data from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-conference-sp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-conference-sp?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-conference-sp?${params}`, {
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
| `conference` | string | no | Optional conference filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conference": "string",
      "defense": {
        "explosiveness": 1,
        "havoc": {
          "db": 1,
          "frontSeven": 1,
          "total": 1
        },
        "passing": 1,
        "passingDowns": 1,
        "rating": 1,
        "rushing": 1,
        "standardDowns": 1,
        "success": 1
      },
      "offense": {
        "explosiveness": 1,
        "pace": 1,
        "passing": 1,
        "passingDowns": 1,
        "rating": 1,
        "runRate": 1,
        "rushing": 1,
        "standardDowns": 1,
        "success": 1
      },
      "rating": 1,
      "secondOrderWins": 1,
      "sos": 1,
      "specialTeams": {
        "rating": 1
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
| `conference` | string |  |
| `defense.explosiveness` | number |  |
| `defense.havoc.db` | number |  |
| `defense.havoc.frontSeven` | number |  |
| `defense.havoc.total` | number |  |
| `defense.passing` | number |  |
| `defense.passingDowns` | number |  |
| `defense.rating` | number |  |
| `defense.rushing` | number |  |
| `defense.standardDowns` | number |  |
| `defense.success` | number |  |
| `offense.explosiveness` | number |  |
| `offense.pace` | number |  |
| `offense.passing` | number |  |
| `offense.passingDowns` | number |  |
| `offense.rating` | number |  |
| `offense.runRate` | number |  |
| `offense.rushing` | number |  |
| `offense.standardDowns` | number |  |
| `offense.success` | number |  |
| `rating` | number |  |
| `secondOrderWins` | number |  |
| `sos` | number |  |
| `specialTeams.rating` | number |  |
| `year` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /ratings/sp/conferences` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conference-sp.md) for the provider-specific parameters and requirements.

