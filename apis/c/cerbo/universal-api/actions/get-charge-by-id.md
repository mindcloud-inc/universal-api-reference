# Cerbo: Get Charge By ID

Retrieves charge details from Cerbo.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/get-charge-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/get-charge-by-id?connectionId=$CONNECTION_ID&charge_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "charge_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/get-charge-by-id?${params}`, {
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
| `charge_id` | number | yes | The ID of the charge to retrieve. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include_deleted` | boolean | no | If true, will return the charge even if it has been deleted. Useful for retrieving historical records. Default: `false`. |

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
        "amt_written_off": "string",
        "cpt_code": "string",
        "cpt_modifiers": "string"
      },
      "charge_master_details": {
        "category": "string",
        "cpt_code": "string",
        "id": 1,
        "name": "Ava Chen",
        "name_for_pt_portal": "Ava Chen",
        "object": "string",
        "retail": "string",
        "wholesale": "string"
      },
      "created": "2026-05-07T12:00:00.000Z",
      "date_deleted": "string",
      "date_voided": "string",
      "discount_multiplier": 1,
      "encounter_id": 1,
      "id": 1,
      "is_deleted": true,
      "is_voided": true,
      "location_identifier": "string",
      "name": "Ava Chen",
      "notes": "string",
      "object": "string",
      "owner_id": 1,
      "patient_id": 1,
      "payment_details": {},
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
| `billing_rules.amt_written_off` | string |  |
| `billing_rules.cpt_code` | string |  |
| `billing_rules.cpt_modifiers` | string |  |
| `charge_master_details` | object |  |
| `charge_master_details.category` | string |  |
| `charge_master_details.cpt_code` | string |  |
| `charge_master_details.id` | number |  |
| `charge_master_details.name` | string |  |
| `charge_master_details.name_for_pt_portal` | string |  |
| `charge_master_details.object` | string |  |
| `charge_master_details.retail` | string |  |
| `charge_master_details.wholesale` | string |  |
| `created` | date |  |
| `date_deleted` | string |  |
| `date_voided` | string |  |
| `discount_multiplier` | number |  |
| `encounter_id` | number |  |
| `id` | number |  |
| `is_deleted` | boolean |  |
| `is_voided` | boolean |  |
| `location_identifier` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `object` | string |  |
| `owner_id` | number |  |
| `patient_id` | number |  |
| `payment_details` | object |  |
| `quantity` | number |  |
| `transaction_date` | date |  |

## Native endpoint

Through the native Cerbo API, this operation is `GET /charges/:charge_id` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-charge-by-id.md) for the provider-specific parameters and requirements.

