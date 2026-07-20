# Pipeline CRM: Retrieve Deal

Retrieves a deal from Pipeline CRM.

```
GET https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/retrieve-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipeline CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/retrieve-deal?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/retrieve-deal?${params}`, {
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
| `id` | number | yes | Deal ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address_1": "string",
      "address_2": "string",
      "city": "string",
      "closed_time": "2026-05-07T12:00:00.000Z",
      "collaborators": [
        {
          "api_key": "string",
          "first_name": "Ava",
          "id": 1,
          "last_name": "Chen"
        }
      ],
      "company_id": 1,
      "company_name": "Ava Chen",
      "company": {
        "id": 1,
        "name": "Ava Chen"
      },
      "country": "string",
      "created_at": "string",
      "currency": {
        "code": "string",
        "name": "Ava Chen",
        "symbol": "string"
      },
      "custom_fields": {},
      "deal_loss_reason_id": 1,
      "deal_loss_reason_notes": "string",
      "deal_loss_reason": {
        "id": 1,
        "name": "Ava Chen"
      },
      "deal_source": 1,
      "deal_stage_id": 1,
      "deal_stage": {
        "id": 1,
        "name": "Ava Chen"
      },
      "deal_won_reason_id": 1,
      "deal_won_reason_notes": "string",
      "expected_close_date": "2026-05-07T12:00:00.000Z",
      "expected_close_date_event_id": 1,
      "id": 1,
      "import_id": 1,
      "is_archived": true,
      "name": "Ava Chen",
      "next_task_all_day": true,
      "next_task_due": "2026-05-07T12:00:00.000Z",
      "next_task_id": 1,
      "next_task_name": "Ava Chen",
      "owner": {
        "full_name": "Ava Chen",
        "id": 1
      },
      "people": [
        {
          "first_name": "Ava",
          "id": 1,
          "last_name": "Chen"
        }
      ],
      "person_ids": [
        [
          1
        ]
      ],
      "possible_notify_user_ids": [
        [
          1
        ]
      ],
      "postal_code": "string",
      "primary_contact_id": 1,
      "primary_contact": {
        "full_name": "Ava Chen",
        "id": 1
      },
      "probability": 1,
      "shared_user_ids": [
        [
          1
        ]
      ],
      "source": {
        "id": 1,
        "name": "Ava Chen"
      },
      "state": "string",
      "status": 1,
      "summary": "string",
      "tag_ids": [
        [
          1
        ]
      ],
      "tags": [
        {
          "id": 1,
          "name": "Ava Chen"
        }
      ],
      "updated_at": "string",
      "user_id": 1,
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address_1` | string |  |
| `address_2` | string |  |
| `city` | string |  |
| `closed_time` | date |  |
| `collaborators[].api_key` | string |  |
| `collaborators[].first_name` | string |  |
| `collaborators[].id` | number |  |
| `collaborators[].last_name` | string |  |
| `company_id` | number |  |
| `company_name` | string |  |
| `company.id` | number |  |
| `company.name` | string |  |
| `country` | string |  |
| `created_at` | string |  |
| `currency.code` | string |  |
| `currency.name` | string |  |
| `currency.symbol` | string |  |
| `custom_fields` | object |  |
| `deal_loss_reason_id` | number |  |
| `deal_loss_reason_notes` | string |  |
| `deal_loss_reason.id` | number |  |
| `deal_loss_reason.name` | string |  |
| `deal_source` | number |  |
| `deal_stage_id` | number |  |
| `deal_stage.id` | number |  |
| `deal_stage.name` | string |  |
| `deal_won_reason_id` | number |  |
| `deal_won_reason_notes` | string |  |
| `expected_close_date` | date |  |
| `expected_close_date_event_id` | number |  |
| `id` | number |  |
| `import_id` | number |  |
| `is_archived` | boolean |  |
| `name` | string |  |
| `next_task_all_day` | boolean |  |
| `next_task_due` | date |  |
| `next_task_id` | number |  |
| `next_task_name` | string |  |
| `owner.full_name` | string |  |
| `owner.id` | number |  |
| `people[].first_name` | string |  |
| `people[].id` | number |  |
| `people[].last_name` | string |  |
| `person_ids[]` | array<number> |  |
| `possible_notify_user_ids[]` | array<number> |  |
| `postal_code` | string |  |
| `primary_contact_id` | number |  |
| `primary_contact.full_name` | string |  |
| `primary_contact.id` | number |  |
| `probability` | number |  |
| `shared_user_ids[]` | array<number> |  |
| `source.id` | number |  |
| `source.name` | string |  |
| `state` | string |  |
| `status` | number |  |
| `summary` | string |  |
| `tag_ids[]` | array<number> |  |
| `tags[].id` | number |  |
| `tags[].name` | string |  |
| `updated_at` | string |  |
| `user_id` | number |  |
| `value` | number |  |

## Native endpoint

Through the native Pipeline CRM API, this operation is `GET /deals/:id` (base URL `https://api.pipelinecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-deal.md) for the provider-specific parameters and requirements.

