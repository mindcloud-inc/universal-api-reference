# OpenFEC: Search Elections

Finds elections in OpenFEC by cycle, office, state, or district.

```
GET https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/search-elections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenFEC `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/search-elections?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/search-elections?${params}`, {
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
| `cycle` | number | no | Two-year election cycle, such as 2024. |
| `office` | string | no | Federal office: president, senate, or house. One of: `0`, `1`, `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "candidate_id": "string",
      "candidate_name": "Ava Chen",
      "cycle": 1,
      "district": "string",
      "election_year": 1,
      "office": "string",
      "party": "string",
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
| `candidate_name` | string |  |
| `cycle` | number |  |
| `district` | string |  |
| `election_year` | number |  |
| `office` | string |  |
| `party` | string |  |
| `state` | string |  |

## Native endpoint

Through the native OpenFEC API, this operation is `GET /elections/search/` (base URL `https://api.open.fec.gov/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-elections.md) for the provider-specific parameters and requirements.

