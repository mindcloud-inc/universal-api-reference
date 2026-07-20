# College Football Data: List Roster

Retrieves historical team rosters from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-roster
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-roster?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-roster?${params}`, {
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
| `year` | number | no | Optional year filter, defaults to 2025 |
| `classification` | string | no | Optional filter to only include players from FBS or FCS teams |

## Response

```json
{
  "success": true,
  "data": [
    {
      "firstName": "Ava",
      "height": 1,
      "homeCity": "string",
      "homeCountry": "string",
      "homeCountyFIPS": "string",
      "homeLatitude": 1,
      "homeLongitude": 1,
      "homeState": "string",
      "id": "string",
      "jersey": 1,
      "lastName": "Chen",
      "position": "string",
      "recruitIds": [
        "string"
      ],
      "team": "string",
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
| `firstName` | string |  |
| `height` | number |  |
| `homeCity` | string |  |
| `homeCountry` | string |  |
| `homeCountyFIPS` | string |  |
| `homeLatitude` | number |  |
| `homeLongitude` | number |  |
| `homeState` | string |  |
| `id` | string |  |
| `jersey` | number |  |
| `lastName` | string |  |
| `position` | string |  |
| `recruitIds` | array<string> |  |
| `team` | string |  |
| `weight` | number |  |
| `year` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /roster` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-roster.md) for the provider-specific parameters and requirements.

