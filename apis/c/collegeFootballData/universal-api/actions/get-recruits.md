# College Football Data: List Recruits

Retrieves player recruiting rankings from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-recruits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-recruits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-recruits?${params}`, {
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
| `year` | number | no | Year filter, required when no team specified |
| `team` | string | no | Team filter, required when no team specified |
| `position` | string | no | Optional position categorization filter |
| `state` | string | no | Optional state/province filter |
| `classification` | string | no | Optional recruit type classification filter, defaults to HighSchool |

## Response

```json
{
  "success": true,
  "data": [
    {
      "athleteId": "string",
      "city": "string",
      "committedTo": "string",
      "country": "string",
      "height": 1,
      "hometownInfo": {
        "fipsCode": "string",
        "latitude": 1,
        "longitude": 1
      },
      "id": "string",
      "name": "Ava Chen",
      "position": "string",
      "ranking": 1,
      "rating": 1,
      "recruitType": "string",
      "school": "string",
      "stars": 1,
      "stateProvince": "string",
      "weight": 1,
      "year": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `athleteId` | string |  |
| `city` | string |  |
| `committedTo` | string |  |
| `country` | string |  |
| `height` | number |  |
| `hometownInfo.fipsCode` | string |  |
| `hometownInfo.latitude` | number |  |
| `hometownInfo.longitude` | number |  |
| `id` | string |  |
| `name` | string |  |
| `position` | string |  |
| `ranking` | number |  |
| `rating` | number |  |
| `recruitType` | string |  |
| `school` | string |  |
| `stars` | number |  |
| `stateProvince` | string |  |
| `weight` | number |  |
| `year` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /recruiting/players` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recruits.md) for the provider-specific parameters and requirements.

