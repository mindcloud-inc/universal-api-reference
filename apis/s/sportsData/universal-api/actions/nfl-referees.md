# SportsData: NFL Referees

Retrieves NFL referees from SportsData.

```
GET https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nfl-referees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SportsData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nfl-referees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nfl-referees?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "college": "string",
      "experience": 1,
      "name": "Ava Chen",
      "number": 1,
      "position": "string",
      "refereeID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `college` | string | College or prior affiliation. |
| `experience` | number | Years of NFL officiating experience. |
| `name` | string | Referee full name. |
| `number` | number | Uniform number. |
| `position` | string | On-field officiating position. |
| `refereeID` | number | SportsData referee identifier. |

## Native endpoint

Through the native SportsData API, this operation is `GET /v3/nfl/scores/json/Referees` (base URL `https://api.sportsdata.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/nfl-referees.md) for the provider-specific parameters and requirements.

