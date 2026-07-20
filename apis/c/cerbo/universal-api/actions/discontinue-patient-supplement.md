# Cerbo: Discontinue Patient Supplement

Discontinues an existing patient supplement in Cerbo.

```
PUT https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/discontinue-patient-supplement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/discontinue-patient-supplement" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pt_id": 1,
  "pt_plan_other_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/discontinue-patient-supplement', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pt_id": 1,
    "pt_plan_other_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pt_id` | number | yes | ID of the patient |
| `pt_plan_other_id` | number | yes | ID of the patient's supplement prescription to discontinue |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `discontinued_date` | date | no | Date and time when the supplement was discontinued. If not provided, defaults to the current date/time. |
| `discontinued_note` | string | no | Reason for discontinuing the supplement |

## Response

```json
{
  "success": true,
  "data": [
    {
      "associated_plan_id": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "encounter_id": 1,
      "id": 1,
      "is_discontinued": true,
      "name": "Ava Chen",
      "object": "string",
      "plan_definition": {
        "class": "string",
        "code": "string",
        "description": "string",
        "disabled": true,
        "id": 1,
        "name": "Ava Chen",
        "nicknames": "Ava Chen"
      },
      "plan_type": "string",
      "prescribing_details": {
        "discontinued": "string",
        "discontinued_date": "2026-05-07T12:00:00.000Z",
        "discontinued_note": "string",
        "dose": "string",
        "frequency": "string",
        "start_date": "string"
      },
      "url_encounter": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `associated_plan_id` | number |  |
| `created` | date |  |
| `encounter_id` | number |  |
| `id` | number |  |
| `is_discontinued` | boolean |  |
| `name` | string |  |
| `object` | string |  |
| `plan_definition` | object |  |
| `plan_definition.class` | string |  |
| `plan_definition.code` | string |  |
| `plan_definition.description` | string |  |
| `plan_definition.disabled` | boolean |  |
| `plan_definition.id` | number |  |
| `plan_definition.name` | string |  |
| `plan_definition.nicknames` | string |  |
| `plan_type` | string |  |
| `prescribing_details` | object |  |
| `prescribing_details.discontinued` | string |  |
| `prescribing_details.discontinued_date` | date |  |
| `prescribing_details.discontinued_note` | string |  |
| `prescribing_details.dose` | string |  |
| `prescribing_details.frequency` | string |  |
| `prescribing_details.start_date` | string |  |
| `url_encounter` | string |  |

## Native endpoint

Through the native Cerbo API, this operation is `PATCH /patients/:pt_id/supplements/:pt_plan_other_id/discontinue` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/discontinue-patient-supplement.md) for the provider-specific parameters and requirements.

