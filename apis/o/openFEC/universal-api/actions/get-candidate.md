# OpenFEC: Get Candidate

Retrieves a candidate from OpenFEC.

```
GET https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/get-candidate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenFEC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/get-candidate?connectionId=$CONNECTION_ID&candidateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "candidateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/get-candidate?${params}`, {
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
      "cycles": [
        1
      ],
      "district": "string",
      "election_years": [
        1
      ],
      "last_file_date": "2026-05-07T12:00:00.000Z",
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
| `cycles` | array<number> |  |
| `district` | string |  |
| `election_years` | array<number> |  |
| `last_file_date` | date |  |
| `name` | string |  |
| `office` | string |  |
| `office_full` | string |  |
| `party` | string |  |
| `party_full` | string |  |
| `state` | string |  |

## Native endpoint

Through the native OpenFEC API, this operation is `GET /candidate/:candidate_id/` (base URL `https://api.open.fec.gov/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-candidate.md) for the provider-specific parameters and requirements.

