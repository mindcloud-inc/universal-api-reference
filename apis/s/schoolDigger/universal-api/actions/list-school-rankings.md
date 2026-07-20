# SchoolDigger: List School Rankings

Retrieves school rankings from SchoolDigger.

```
GET https://connect.mindcloud.co/v1/universal/schoolDigger/latest/actions/list-school-rankings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SchoolDigger `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/schoolDigger/latest/actions/list-school-rankings?connectionId=$CONNECTION_ID&limit=25&offset=0&st=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "st": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/schoolDigger/latest/actions/list-school-rankings?${params}`, {
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
| `st` | string | yes | Two-letter state code for the ranking list. |
| `year` | number | no | Ranking year. Defaults to the most recent year when omitted. |
| `level` | list | no | Ranking level: Elementary, Middle, or High. One of: `0`, `1`, `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "district": {},
      "isPrivate": true,
      "rankHistory": [
        {}
      ],
      "rankMovement": 1,
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
| `district` | object |  |
| `isPrivate` | boolean |  |
| `rankHistory` | array<object> |  |
| `rankMovement` | number |  |
| `schoolid` | string |  |
| `schoolLevel` | string |  |
| `schoolName` | string |  |
| `schoolYearlyDetails` | array<object> |  |
| `url` | string |  |

## Native endpoint

Through the native SchoolDigger API, this operation is `GET /rankings/schools/:st` (base URL `https://api.schooldigger.com/v2.3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-school-rankings.md) for the provider-specific parameters and requirements.

