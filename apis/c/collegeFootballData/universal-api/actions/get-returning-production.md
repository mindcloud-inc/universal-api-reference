# College Football Data: List Returning Production

Retrieves returning production data from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-returning-production
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-returning-production?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-returning-production?${params}`, {
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
| `conference` | string | no | Optional conference filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conference": "string",
      "passingUsage": 1,
      "percentPassingPPA": 1,
      "percentPPA": 1,
      "percentReceivingPPA": 1,
      "percentRushingPPA": 1,
      "receivingUsage": 1,
      "rushingUsage": 1,
      "season": 1,
      "team": "string",
      "totalPassingPPA": 1,
      "totalPPA": 1,
      "totalReceivingPPA": 1,
      "totalRushingPPA": 1,
      "usage": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conference` | string |  |
| `passingUsage` | number |  |
| `percentPassingPPA` | number |  |
| `percentPPA` | number |  |
| `percentReceivingPPA` | number |  |
| `percentRushingPPA` | number |  |
| `receivingUsage` | number |  |
| `rushingUsage` | number |  |
| `season` | number |  |
| `team` | string |  |
| `totalPassingPPA` | number |  |
| `totalPPA` | number |  |
| `totalReceivingPPA` | number |  |
| `totalRushingPPA` | number |  |
| `usage` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /player/returning` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-returning-production.md) for the provider-specific parameters and requirements.

