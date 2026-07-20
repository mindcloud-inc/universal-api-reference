# College Football Data: Search Players

Finds players in College Football Data by name.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/search-players
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/search-players?connectionId=$CONNECTION_ID&searchTerm=Alabama" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchTerm": "Alabama"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/search-players?${params}`, {
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
| `searchTerm` | string | yes | Search term for matching player name Default: `Alabama`. |
| `year` | number | no | Optional year filter |
| `team` | string | no | Optional team filter |
| `position` | string | no | Optional position abbreviation filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "firstName": "Ava",
      "height": 1,
      "hometown": "string",
      "id": "string",
      "jersey": 1,
      "lastName": "Chen",
      "name": "Ava Chen",
      "position": "string",
      "team": "string",
      "teamColor": "string",
      "teamColorSecondary": "string",
      "weight": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `firstName` | string |  |
| `height` | number |  |
| `hometown` | string |  |
| `id` | string |  |
| `jersey` | number |  |
| `lastName` | string |  |
| `name` | string |  |
| `position` | string |  |
| `team` | string |  |
| `teamColor` | string |  |
| `teamColorSecondary` | string |  |
| `weight` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /player/search` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-players.md) for the provider-specific parameters and requirements.

