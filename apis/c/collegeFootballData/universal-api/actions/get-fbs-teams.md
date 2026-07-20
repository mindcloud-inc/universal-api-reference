# College Football Data: List F B S Teams

Retrieves FBS teams from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-fbs-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-fbs-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-fbs-teams?${params}`, {
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
| `year` | number | no | Year or season |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abbreviation": "string",
      "alternateColor": "string",
      "alternateNames": [
        "Ava Chen"
      ],
      "classification": "string",
      "color": "string",
      "conference": "string",
      "division": "string",
      "id": 1,
      "location": {
        "capacity": 1,
        "city": "string",
        "constructionYear": 1,
        "countryCode": "string",
        "dome": true,
        "elevation": "string",
        "grass": true,
        "id": 1,
        "latitude": 1,
        "longitude": 1,
        "name": "Ava Chen",
        "state": "string",
        "timezone": "string",
        "zip": "string"
      },
      "logos": [
        "string"
      ],
      "mascot": "string",
      "school": "string",
      "twitter": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abbreviation` | string |  |
| `alternateColor` | string |  |
| `alternateNames` | array<string> |  |
| `classification` | string |  |
| `color` | string |  |
| `conference` | string |  |
| `division` | string |  |
| `id` | number |  |
| `location.capacity` | number |  |
| `location.city` | string |  |
| `location.constructionYear` | number |  |
| `location.countryCode` | string |  |
| `location.dome` | boolean |  |
| `location.elevation` | string |  |
| `location.grass` | boolean |  |
| `location.id` | number |  |
| `location.latitude` | number |  |
| `location.longitude` | number |  |
| `location.name` | string |  |
| `location.state` | string |  |
| `location.timezone` | string |  |
| `location.zip` | string |  |
| `logos` | array<string> |  |
| `mascot` | string |  |
| `school` | string |  |
| `twitter` | string |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /teams/fbs` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fbs-teams.md) for the provider-specific parameters and requirements.

