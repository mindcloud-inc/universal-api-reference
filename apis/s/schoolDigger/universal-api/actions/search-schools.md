# SchoolDigger: Search Schools

Finds schools in SchoolDigger by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/schoolDigger/latest/actions/search-schools
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SchoolDigger `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/schoolDigger/latest/actions/search-schools?connectionId=$CONNECTION_ID&limit=25&offset=0&st=WA" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "st": "WA"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/schoolDigger/latest/actions/search-schools?${params}`, {
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
| `city` | string | no | Filter schools by city. |
| `districtID` | string | no | Filter schools to a SchoolDigger district ID. |
| `q` | string | no | School name or city search term. Default: `Lincoln`. |
| `st` | string | yes | Two-letter state code, such as WA or NJ. Default: `WA`. |
| `zip` | string | no | Filter schools by five-digit ZIP code. |
| `level` | list | no | School level filter. One of: `0`, `1`, `2`, `3`, `4`, `5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "county": {},
      "district": {},
      "highGrade": "string",
      "isPrivate": true,
      "lowGrade": "string",
      "phone": "string",
      "rankHistory": [
        {}
      ],
      "schoolid": "string",
      "schoolLevel": "string",
      "schoolName": "Ava Chen",
      "schoolYearlyDetails": [
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
| `district` | object |  |
| `highGrade` | string |  |
| `isPrivate` | boolean |  |
| `lowGrade` | string |  |
| `phone` | string |  |
| `rankHistory` | array<object> |  |
| `schoolid` | string | SchoolDigger school ID. |
| `schoolLevel` | string |  |
| `schoolName` | string |  |
| `schoolYearlyDetails` | array<object> |  |
| `url` | string |  |

## Native endpoint

Through the native SchoolDigger API, this operation is `GET /schools` (base URL `https://api.schooldigger.com/v2.3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-schools.md) for the provider-specific parameters and requirements.

