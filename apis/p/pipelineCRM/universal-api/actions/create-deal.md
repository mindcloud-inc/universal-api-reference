# Pipeline CRM: Create Deal

Creates a new deal in Pipeline CRM.

```
POST https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/create-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipeline CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/create-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/create-deal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deliverAssignmentEmail` | boolean | no | Send an assignment email when the deal is assigned to another user. Default: `true`. |
| `deal.name` | string | no | The name of the deal. |
| `deal.summary` | string | no | Explanatory or descriptive text about the deal. |
| `deal.userId` | number | no | The ID of the user who owns this deal. |
| `deal.status` | number | no | The deal status ID for this deal. |
| `deal.expectedCloseDate` | date | no | The date the deal is expected to close by (YYYY-MM-DD). |
| `deal.value` | number | no | The deal's value in its currency. |
| `deal.primaryContactId` | number | no | The primary contact person ID associated with this deal. |
| `deal.personIds[]` | array<number> | no | Person record IDs associated with this deal. |
| `deal.companyId` | number | no | The company ID associated with this deal. |
| `deal.companyName` | string | no | Creates or associates a company with this deal by name. |
| `deal.probability` | number | no | Probability from 0-100 that the deal will close. |
| `deal.dealStageId` | number | no | The deal stage ID for this deal. |
| `deal.dealLossReasonId` | number | no | The deal loss reason ID for this deal. |
| `deal.dealWonReasonId` | number | no | The deal won reason ID for this deal. |
| `deal.dealSource` | number | no | The lead source ID for this deal. |
| `deal.tagIds[]` | array<number> | no | Tag IDs to set on this deal. |
| `todoTemplateId` | number | no | The todo template ID to apply to this deal. |
| `todoTemplateUserId` | number | no | The owner of tasks created from the todo template. |

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

Through the native Pipeline CRM API, this operation is `POST /deals` (base URL `https://api.pipelinecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deal.md) for the provider-specific parameters and requirements.

