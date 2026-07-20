# OpenFEC: Get Committee

Retrieves a committee from OpenFEC.

```
GET https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/get-committee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenFEC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/get-committee?connectionId=$CONNECTION_ID&committeeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "committeeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/get-committee?${params}`, {
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

Through the native OpenFEC API, this operation is `GET /committee/:committee_id/` (base URL `https://api.open.fec.gov/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-committee.md) for the provider-specific parameters and requirements.

