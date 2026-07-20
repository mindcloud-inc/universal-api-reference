# Cerbo: List Patient Specialists

Retrieves patient specialists from Cerbo.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-patient-specialists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-patient-specialists?connectionId=$CONNECTION_ID&patient_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "patient_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-patient-specialists?${params}`, {
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
| `patient_id` | number | yes | The patient ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedby": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "note": "string",
      "object": "string",
      "priority_order": 1,
      "specialist_details": {
        "address1": "string",
        "city": "string",
        "email": "ava@example.com",
        "fax": "string",
        "id": 1,
        "name": "Ava Chen",
        "phone": "string",
        "specialty": "string",
        "state": "string",
        "zip": "string"
      },
      "specialist_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedby` | number |  |
| `created` | date |  |
| `id` | number |  |
| `note` | string |  |
| `object` | string |  |
| `priority_order` | number |  |
| `specialist_details` | object |  |
| `specialist_details.address1` | string |  |
| `specialist_details.city` | string |  |
| `specialist_details.email` | string |  |
| `specialist_details.fax` | string |  |
| `specialist_details.id` | number |  |
| `specialist_details.name` | string |  |
| `specialist_details.phone` | string |  |
| `specialist_details.specialty` | string |  |
| `specialist_details.state` | string |  |
| `specialist_details.zip` | string |  |
| `specialist_id` | number |  |

## Native endpoint

Through the native Cerbo API, this operation is `GET /patients/:patient_id/specialists` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-patient-specialists.md) for the provider-specific parameters and requirements.

