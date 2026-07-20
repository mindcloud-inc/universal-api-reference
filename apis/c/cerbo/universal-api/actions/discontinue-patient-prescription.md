# Cerbo: Discontinue Patient Prescription

Discontinues an existing patient prescription in Cerbo.

```
PUT https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/discontinue-patient-prescription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/discontinue-patient-prescription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pt_id": 1,
  "pt_rx_id": 1,
  "discontinued_reason": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/discontinue-patient-prescription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pt_id": 1,
    "pt_rx_id": 1,
    "discontinued_reason": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pt_id` | number | yes | ID of the patient |
| `pt_rx_id` | number | yes | ID of the patient's medication prescription to discontinue |
| `discontinued_reason` | string | yes | Reason for discontinuing the medication (required) |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `discontinued_date` | date | no | Date and time when the medication was discontinued. If not provided, defaults to the current date/time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "discontinued_date": "2026-05-07T12:00:00.000Z",
      "discontinued_reason": "string",
      "drug_id": 1,
      "drug_name": "Ava Chen",
      "id": 1,
      "object": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `discontinued_date` | date |  |
| `discontinued_reason` | string |  |
| `drug_id` | number |  |
| `drug_name` | string |  |
| `id` | number |  |
| `object` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Cerbo API, this operation is `PATCH /patients/:pt_id/rxs/:pt_rx_id/discontinue` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/discontinue-patient-prescription.md) for the provider-specific parameters and requirements.

