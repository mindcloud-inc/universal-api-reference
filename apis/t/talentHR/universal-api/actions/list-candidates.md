# TalentHR: List Candidates

Retrieves candidates from TalentHR.

```
GET https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-candidates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentHR `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-candidates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-candidates?${params}`, {
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
| `limit` | number | no | Maximum number of candidates to return. |
| `offset` | number | no | Number of candidates to skip before returning results. |
| `search` | string | no | Free-text search term for candidates. |
| `sort` | string | no | Field used to sort candidate results. |
| `order` | string | no | Sort direction for candidate results. |
| `pool` | boolean | no | Whether to restrict results to the talent pool. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "rows": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rows` | array<object> |  |
| `total` | number |  |

## Native endpoint

Through the native TalentHR API, this operation is `GET /ats-applicants` (base URL `https://pubapi.talenthr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-candidates.md) for the provider-specific parameters and requirements.

