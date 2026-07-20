# SchoolDigger: Autocomplete Districts

Finds district matches in SchoolDigger by partial search text.

```
GET https://connect.mindcloud.co/v1/universal/schoolDigger/latest/actions/autocomplete-districts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SchoolDigger `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/schoolDigger/latest/actions/autocomplete-districts?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/schoolDigger/latest/actions/autocomplete-districts?${params}`, {
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
| `q` | string | yes | Autocomplete search term. |
| `st` | string | no | Optional two-letter state code filter. |
| `returnCount` | number | no | Number of autocomplete matches to return, from 1 to 20. Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "districtid": "string",
      "districtName": "Ava Chen",
      "hasBoundary": true,
      "highGrade": "string",
      "latitude": 1,
      "longitude": 1,
      "lowGrade": "string",
      "rank": 1,
      "rankOf": 1,
      "rankStars": 1,
      "state": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `districtid` | string |  |
| `districtName` | string |  |
| `hasBoundary` | boolean |  |
| `highGrade` | string |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `lowGrade` | string |  |
| `rank` | number |  |
| `rankOf` | number |  |
| `rankStars` | number |  |
| `state` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native SchoolDigger API, this operation is `GET /autocomplete/districts` (base URL `https://api.schooldigger.com/v2.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/autocomplete-districts.md) for the provider-specific parameters and requirements.

