# OpenFEC: List Committee History

Retrieves a committee's history from OpenFEC.

```
GET https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-committee-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenFEC `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-committee-history?connectionId=$CONNECTION_ID&limit=25&offset=0&committeeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "committeeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-committee-history?${params}`, {
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
| `committeeId` | string | yes | FEC committee ID, such as C00580100. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "committee_id": "string",
      "committee_type": "string",
      "committee_type_full": "string",
      "cycle": 1,
      "designation": "string",
      "designation_full": "string",
      "name": "Ava Chen",
      "party": "string",
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
| `cycle` | number |  |
| `designation` | string |  |
| `designation_full` | string |  |
| `name` | string |  |
| `party` | string |  |
| `state` | string |  |
| `treasurer_name` | string |  |

## Native endpoint

Through the native OpenFEC API, this operation is `GET /committee/:committee_id/history/` (base URL `https://api.open.fec.gov/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-committee-history.md) for the provider-specific parameters and requirements.

