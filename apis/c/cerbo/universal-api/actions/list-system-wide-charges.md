# Cerbo: List System-Wide Charges

Retrieves system-wide charges from Cerbo.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-system-wide-charges
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-system-wide-charges?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-system-wide-charges?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `date_method` | string | no | If filtering by date range, should the range be calculated by date the charge was created, or the recorded transaction date? Valid arguments are 'created' and 'transaction' (created is the default). Default: `created`. |
| `start_date` | date | no | Show charges from after this date (calculated by date_method). |
| `end_date` | date | no | Show charges from before this date (calculated by date_method). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedby": 1,
      "additional_details": "string",
      "amount": "string",
      "billing_rules": {},
      "charge_master_details": {},
      "created": "2026-05-07T12:00:00.000Z",
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
| `charge_master_details` | object |  |
| `created` | date |  |
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

Through the native Cerbo API, this operation is `GET /charges` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-system-wide-charges.md) for the provider-specific parameters and requirements.

