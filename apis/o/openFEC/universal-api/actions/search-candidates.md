# OpenFEC: Search Candidates

Finds candidates in OpenFEC by search terms.

```
GET https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/search-candidates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenFEC `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/search-candidates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/search-candidates?${params}`, {
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
| `q` | string | no | Candidate name search text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "candidate_id": "string",
      "cycles": [
        1
      ],
      "district": "string",
      "name": "Ava Chen",
      "office": "string",
      "office_full": "string",
      "party": "string",
      "party_full": "string",
      "principal_committees": [
        {}
      ],
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `candidate_id` | string |  |
| `cycles` | array<number> |  |
| `district` | string |  |
| `name` | string |  |
| `office` | string |  |
| `office_full` | string |  |
| `party` | string |  |
| `party_full` | string |  |
| `principal_committees` | array<object> |  |
| `state` | string |  |

## Native endpoint

Through the native OpenFEC API, this operation is `GET /candidates/search/` (base URL `https://api.open.fec.gov/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-candidates.md) for the provider-specific parameters and requirements.

