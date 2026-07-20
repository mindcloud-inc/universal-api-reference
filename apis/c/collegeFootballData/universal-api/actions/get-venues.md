# College Football Data: List Venues

Retrieves venues from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-venues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-venues?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-venues?${params}`, {
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capacity` | number |  |
| `city` | string |  |
| `constructionYear` | number |  |
| `countryCode` | string |  |
| `dome` | boolean |  |
| `elevation` | string |  |
| `grass` | boolean |  |
| `id` | number |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `name` | string |  |
| `state` | string |  |
| `timezone` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /venues` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-venues.md) for the provider-specific parameters and requirements.

