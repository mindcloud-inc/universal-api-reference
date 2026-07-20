# College Football Data: List Transfer Portal

Retrieves transfer portal entries from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-transfer-portal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-transfer-portal?connectionId=$CONNECTION_ID&year=2025" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "year": "2025"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-transfer-portal?${params}`, {
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
| `year` | number | yes | Required year filter Default: `2025`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "destination": "string",
      "eligibility": "string",
      "firstName": "Ava",
      "lastName": "Chen",
      "origin": "string",
      "position": "string",
      "rating": 1,
      "season": 1,
      "stars": 1,
      "transferDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `destination` | string |  |
| `eligibility` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `origin` | string |  |
| `position` | string |  |
| `rating` | number |  |
| `season` | number |  |
| `stars` | number |  |
| `transferDate` | string |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /player/portal` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transfer-portal.md) for the provider-specific parameters and requirements.

