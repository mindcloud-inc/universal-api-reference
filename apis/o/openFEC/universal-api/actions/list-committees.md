# OpenFEC: List Committees

Retrieves a list of committees from OpenFEC.

```
GET https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-committees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenFEC `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-committees?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-committees?${params}`, {
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
| `q` | string | no | Committee name search text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "committee_id": "string",
      "committee_type": "string",
      "committee_type_full": "string",
      "cycles": [
        1
      ],
      "designation": "string",
      "designation_full": "string",
      "name": "Ava Chen",
      "organization_type_full": "string",
      "party": "string",
      "party_full": "string",
      "state": "string",
      "treasurer_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `committee_id` | string |  |
| `committee_type` | string |  |
| `committee_type_full` | string |  |
| `cycles` | array<number> |  |
| `designation` | string |  |
| `designation_full` | string |  |
| `name` | string |  |
| `organization_type_full` | string |  |
| `party` | string |  |
| `party_full` | string |  |
| `state` | string |  |
| `treasurer_name` | string |  |

## Native endpoint

Through the native OpenFEC API, this operation is `GET /committees/` (base URL `https://api.open.fec.gov/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-committees.md) for the provider-specific parameters and requirements.

