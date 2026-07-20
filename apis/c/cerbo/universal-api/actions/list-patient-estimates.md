# Cerbo: List Patient Estimates

Retrieves patient estimates from Cerbo.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-patient-estimates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-patient-estimates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-patient-estimates?${params}`, {
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
| `patientId` | number | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `date_method` | string | no | If you're filtering by date range, should the range be calculated by date the estimated charge was created, or the recorded transaction date (manual date assigned to the estimated charge)? Valid arguments are *created* and *transaction* (created is the default). |
| `start_date` | date | no | If this argument is included it will only show estimated charges from after this date (calculated by `date_method`). |
| `end_date` | date | no | If this argument is included it will only show estimated charges from before this date (calculated by `date_method`). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedby": 1,
      "additional_details": "string",
      "amount": "string",
      "billing_rules": {
        "add_to_insurance_claim": true,
        "amt_billed_to_insurance": "string",
        "amt_paid_by_insurance": "string",
        "cpt_code": "string",
        "cpt_modifiers": "string",
        "date_paid_by_insurance": "string",
        "justifying_diagnoses": [
          "string"
        ],
        "which_insurance_to_bill": "string"
      },
      "charge_master_details": {},
      "converted_tp_patient_charge_id": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "date_deleted": "2026-05-07T12:00:00.000Z",
      "discount_multiplier": 1,
      "encounter_id": 1,
      "expiration_date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "is_deleted": true,
      "location_identifier": "string",
      "name": "Ava Chen",
      "notes": "string",
      "object": "string",
      "owner_id": 1,
      "patient_id": 1,
      "payment_details": "string",
      "quantity": 1,
      "transaction_date": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedby` | number |  |
| `additional_details` | string |  |
| `amount` | string |  |
| `billing_rules` | object |  |
| `billing_rules.add_to_insurance_claim` | boolean |  |
| `billing_rules.amt_billed_to_insurance` | string |  |
| `billing_rules.amt_paid_by_insurance` | string |  |
| `billing_rules.cpt_code` | string |  |
| `billing_rules.cpt_modifiers` | string |  |
| `billing_rules.date_paid_by_insurance` | string |  |
| `billing_rules.justifying_diagnoses` | array<string> |  |
| `billing_rules.which_insurance_to_bill` | string |  |
| `charge_master_details` | object |  |
| `converted_tp_patient_charge_id` | string |  |
| `created` | date |  |
| `date_deleted` | date |  |
| `discount_multiplier` | number |  |
| `encounter_id` | number |  |
| `expiration_date` | date |  |
| `id` | number |  |
| `is_deleted` | boolean |  |
| `location_identifier` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `object` | string |  |
| `owner_id` | number |  |
| `patient_id` | number |  |
| `payment_details` | string |  |
| `quantity` | number |  |
| `transaction_date` | date |  |

## Native endpoint

Through the native Cerbo API, this operation is `GET /patients/:pt_id/estimates` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-patient-estimates.md) for the provider-specific parameters and requirements.

