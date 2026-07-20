# OpenFEC: List Candidate History

Retrieves a candidate's history from OpenFEC.

```
GET https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-candidate-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenFEC `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-candidate-history?connectionId=$CONNECTION_ID&limit=25&offset=0&candidateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "candidateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-candidate-history?${params}`, {
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
| `candidateId` | string | yes | FEC candidate ID, such as P80000722. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "candidate_id": "string",
      "candidate_status": "string",
      "cycle": 1,
      "district": "string",
      "name": "Ava Chen",
      "office": "string",
      "office_full": "string",
      "party": "string",
      "party_full": "string",
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
| `candidate_status` | string |  |
| `cycle` | number |  |
| `district` | string |  |
| `name` | string |  |
| `office` | string |  |
| `office_full` | string |  |
| `party` | string |  |
| `party_full` | string |  |
| `state` | string |  |

## Native endpoint

Through the native OpenFEC API, this operation is `GET /candidate/:candidate_id/history/` (base URL `https://api.open.fec.gov/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-candidate-history.md) for the provider-specific parameters and requirements.

