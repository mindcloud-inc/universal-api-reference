# SchoolDigger: Search Districts

Finds districts in SchoolDigger by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/schoolDigger/latest/actions/search-districts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SchoolDigger `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/schoolDigger/latest/actions/search-districts?connectionId=$CONNECTION_ID&limit=25&offset=0&st=WA" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "st": "WA"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/schoolDigger/latest/actions/search-districts?${params}`, {
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
| `city` | string | no | Filter districts by city. |
| `q` | string | no | District name or city search term. Default: `Seattle`. |
| `st` | string | yes | Two-letter state code, such as WA or NJ. Default: `WA`. |
| `zip` | string | no | Filter districts by five-digit ZIP code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "county": {},
      "districtID": "string",
      "districtName": "Ava Chen",
      "districtYearlyDetails": [
        {}
      ],
      "numberHighSchools": 1,
      "numberMiddleSchools": 1,
      "numberPrimarySchools": 1,
      "numberTotalSchools": 1,
      "phone": "string",
      "rankHistory": [
        {}
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `county` | object |  |
| `districtID` | string |  |
| `districtName` | string |  |
| `districtYearlyDetails` | array<object> |  |
| `numberHighSchools` | number |  |
| `numberMiddleSchools` | number |  |
| `numberPrimarySchools` | number |  |
| `numberTotalSchools` | number |  |
| `phone` | string |  |
| `rankHistory` | array<object> |  |
| `url` | string |  |

## Native endpoint

Through the native SchoolDigger API, this operation is `GET /districts` (base URL `https://api.schooldigger.com/v2.3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-districts.md) for the provider-specific parameters and requirements.

