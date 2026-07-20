# Freshworks CRM: Create Manual Call Log

Creates a manual call log in Freshworks CRM.

```
POST https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-manual-call-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-manual-call-log" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phoneCall": {},
  "phoneCall.callDirection": true,
  "phoneCall.targetable": {},
  "phoneCall.targetableType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-manual-call-log', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phoneCall": {},
    "phoneCall.callDirection": true,
    "phoneCall.targetable": {},
    "phoneCall.targetableType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phoneCall` | object | yes | Manual call log payload |
| `phoneCall.callDirection` | boolean | yes | Directional flag for the manual call log |
| `phoneCall.note` | object | no | Optional note payload |
| `phoneCall.targetable` | object | yes | Linked contact/account payload |
| `phoneCall.targetableType` | string | yes | Entity type for the linked record |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appointments": [
        [
          {}
        ]
      ],
      "contacts": [
        [
          {}
        ]
      ],
      "currencies": [
        [
          {}
        ]
      ],
      "deal_payment_statuses": [
        [
          {}
        ]
      ],
      "deal_pipelines": [
        [
          {}
        ]
      ],
      "deal_stages": [
        [
          {}
        ]
      ],
      "deals": [
        [
          {}
        ]
      ],
      "lead_sources": [
        [
          {}
        ]
      ],
      "notes": [
        [
          {}
        ]
      ],
      "phone_calls": [
        [
          {}
        ]
      ],
      "sales_accounts": [
        [
          {}
        ]
      ],
      "sales_activity_entity_types": [
        [
          {}
        ]
      ],
      "targetables": [
        [
          {}
        ]
      ],
      "tasks": [
        [
          {}
        ]
      ],
      "user": [
        [
          {}
        ]
      ],
      "users": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appointments[]` | array<object> |  |
| `appointments[].appointment_attendee_ids[]` | array<number> |  |
| `appointments[].can_checkin` | boolean |  |
| `appointments[].can_checkin_checkout` | boolean |  |
| `appointments[].created_at` | date |  |
| `appointments[].creater_id` | number |  |
| `appointments[].description` | string |  |
| `appointments[].end_date` | date |  |
| `appointments[].from_date` | date |  |
| `appointments[].has_multiple_emails` | boolean |  |
| `appointments[].id` | number |  |
| `appointments[].is_allday` | boolean |  |
| `appointments[].location` | string |  |
| `appointments[].note_id` | number |  |
| `appointments[].provider` | string |  |
| `appointments[].targetable_ids[]` | array<number> |  |
| `appointments[].targetable.id` | number |  |
| `appointments[].targetable.type` | string |  |
| `appointments[].targetables_with_email[]` | array<object> |  |
| `appointments[].targetables[]` | array<object> |  |
| `appointments[].targetables[].id` | number |  |
| `appointments[].targetables[].type` | string |  |
| `appointments[].time_zone` | string |  |
| `appointments[].title` | string |  |
| `appointments[].updated_at` | date |  |
| `appointments[].updater_id` | number |  |
| `contacts[]` | array<object> |  |
| `contacts[].avatar` | string |  |
| `contacts[].deal_ids[]` | array<number> |  |
| `contacts[].display_name` | string |  |
| `contacts[].email` | string |  |
| `contacts[].first_name` | string |  |
| `contacts[].has_access` | boolean |  |
| `contacts[].id` | number |  |
| `contacts[].job_title` | string |  |
| `contacts[].last_name` | string |  |
| `contacts[].last_seen` | date |  |
| `contacts[].lead_score` | number |  |
| `contacts[].mobile_number` | string |  |
| `contacts[].owner_id` | number |  |
| `contacts[].partial` | boolean |  |
| `contacts[].record_type_id` | string |  |
| `contacts[].sales_accounts[]` | array<object> |  |
| `contacts[].sales_accounts[].avatar` | string |  |
| `contacts[].sales_accounts[].id` | number |  |
| `contacts[].sales_accounts[].is_primary` | boolean |  |
| `contacts[].sales_accounts[].last_contacted` | date |  |
| `contacts[].sales_accounts[].name` | string |  |
| `contacts[].sales_accounts[].open_deals_amount` | string |  |
| `contacts[].sales_accounts[].open_deals_count` | number |  |
| `contacts[].sales_accounts[].partial` | boolean |  |
| `contacts[].sales_accounts[].record_type_id` | string |  |
| `contacts[].sales_accounts[].website` | string |  |
| `contacts[].sales_accounts[].won_deals_amount` | string |  |
| `contacts[].sales_accounts[].won_deals_count` | number |  |
| `contacts[].work_number` | string |  |
| `currencies[]` | array<object> |  |
| `currencies[].currency_code` | string |  |
| `currencies[].currency_type` | number |  |
| `currencies[].exchange_rate` | string |  |
| `currencies[].id` | number |  |
| `currencies[].is_active` | boolean |  |
| `currencies[].partial` | boolean |  |
| `currencies[].rate_change_ids[]` | array<number> |  |
| `deal_payment_statuses[]` | array<object> |  |
| `deal_payment_statuses[].id` | number |  |
| `deal_payment_statuses[].name` | string |  |
| `deal_payment_statuses[].partial` | boolean |  |
| `deal_payment_statuses[].position` | number |  |
| `deal_pipelines[]` | array<object> |  |
| `deal_pipelines[].aggregated_field` | string |  |
| `deal_pipelines[].configs[]` | array<object> |  |
| `deal_pipelines[].configs[].field_name` | string |  |
| `deal_pipelines[].configs[].highlight` | boolean |  |
| `deal_pipelines[].configs[].position` | number |  |
| `deal_pipelines[].id` | number |  |
| `deal_pipelines[].is_default` | boolean |  |
| `deal_pipelines[].name` | string |  |
| `deal_pipelines[].partial` | boolean |  |
| `deal_pipelines[].position` | number |  |
| `deal_pipelines[].rotting_days` | number |  |
| `deal_stages[]` | array<object> |  |
| `deal_stages[].choice_type` | number |  |
| `deal_stages[].deal_pipeline_id` | number |  |
| `deal_stages[].forecast_type` | string |  |
| `deal_stages[].id` | number |  |
| `deal_stages[].name` | string |  |
| `deal_stages[].partial` | boolean |  |
| `deal_stages[].position` | number |  |
| `deal_stages[].probability` | number |  |
| `deal_stages[].updated_at` | date |  |
| `deals[]` | array<object> |  |
| `deals[].amount` | string |  |
| `deals[].deal_pipeline_id` | number |  |
| `deals[].deal_stage_id` | number |  |
| `deals[].has_access` | boolean |  |
| `deals[].id` | number |  |
| `deals[].name` | string |  |
| `deals[].partial` | boolean |  |
| `deals[].record_type_id` | string |  |
| `lead_sources[]` | array<object> |  |
| `lead_sources[].id` | number |  |
| `lead_sources[].name` | string |  |
| `lead_sources[].partial` | boolean |  |
| `lead_sources[].position` | number |  |
| `notes[]` | array<object> |  |
| `notes[].collab_context.hasSlackViewAccess` | boolean |  |
| `notes[].collab_context.messageId` | string |  |
| `notes[].created_at` | date |  |
| `notes[].creater_id` | number |  |
| `notes[].description` | string |  |
| `notes[].has_access` | boolean |  |
| `notes[].has_mentions` | boolean |  |
| `notes[].html_content` | string |  |
| `notes[].id` | number |  |
| `notes[].source_id` | number |  |
| `notes[].source_type` | string |  |
| `notes[].targetable.id` | number |  |
| `notes[].targetable.type` | string |  |
| `notes[].targetables[]` | array<object> |  |
| `notes[].targetables[].id` | number |  |
| `notes[].targetables[].type` | string |  |
| `notes[].updated_at` | date |  |
| `phone_calls[]` | array<object> |  |
| `phone_calls[].call_direction` | boolean |  |
| `phone_calls[].conversation_time` | date |  |
| `phone_calls[].cost` | number |  |
| `phone_calls[].id` | number |  |
| `phone_calls[].is_external_recording_url` | boolean |  |
| `phone_calls[].is_manual` | boolean |  |
| `phone_calls[].note_id` | number |  |
| `phone_calls[].root_phone_call_id` | number |  |
| `phone_calls[].status` | string |  |
| `phone_calls[].targetable.id` | number |  |
| `phone_calls[].targetable.type` | string |  |
| `phone_calls[].user_id` | number |  |
| `sales_accounts[]` | array<object> |  |
| `sales_accounts[].has_access` | boolean |  |
| `sales_accounts[].id` | number |  |
| `sales_accounts[].name` | string |  |
| `sales_accounts[].partial` | boolean |  |
| `sales_accounts[].phone` | string |  |
| `sales_accounts[].record_type_id` | string |  |
| `sales_activity_entity_types[]` | array<object> |  |
| `sales_activity_entity_types[].id` | number |  |
| `sales_activity_entity_types[].name` | string |  |
| `sales_activity_entity_types[].partial` | boolean |  |
| `sales_activity_entity_types[].position` | number |  |
| `sales_activity_entity_types[].sales_activity_type_id` | number |  |
| `targetables[]` | array<object> |  |
| `targetables[].targetable.id` | number |  |
| `targetables[].targetable.type` | string |  |
| `tasks[]` | array<object> |  |
| `tasks[].created_at` | date |  |
| `tasks[].creater_id` | number |  |
| `tasks[].description` | string |  |
| `tasks[].due_date` | date |  |
| `tasks[].has_multiple_emails` | boolean |  |
| `tasks[].id` | number |  |
| `tasks[].is_linkedin_type` | boolean |  |
| `tasks[].owner_id` | number |  |
| `tasks[].status` | number |  |
| `tasks[].targetable_ids[]` | array<number> |  |
| `tasks[].targetable.id` | number |  |
| `tasks[].targetable.type` | string |  |
| `tasks[].targetables_with_email[]` | array<object> |  |
| `tasks[].targetables[]` | array<object> |  |
| `tasks[].targetables[].id` | number |  |
| `tasks[].targetables[].type` | string |  |
| `tasks[].task_type_id` | number |  |
| `tasks[].title` | string |  |
| `tasks[].updated_at` | date |  |
| `tasks[].updater_id` | number |  |
| `tasks[].user_ids[]` | array<number> |  |
| `user[]` | array<object> |  |
| `user[].display_name` | string |  |
| `user[].email` | string |  |
| `user[].id` | number |  |
| `user[].is_active` | boolean |  |
| `user[].work_number` | string |  |
| `users[]` | array<object> |  |
| `users[].display_name` | string |  |
| `users[].email` | string |  |
| `users[].id` | number |  |
| `users[].is_active` | boolean |  |
| `users[].partial` | boolean |  |
| `users[].user_profile_attributes.id` | number |  |
| `users[].user_profile_attributes.is_active` | boolean |  |
| `users[].user_profile_attributes.mobile_number` | string |  |
| `users[].user_profile_attributes.work_number` | string |  |
| `users[].uuid` | string |  |
| `users[].work_number` | string |  |

## Native endpoint

Through the native Freshworks CRM API, this operation is `POST /api/phone_calls` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-manual-call-log.md) for the provider-specific parameters and requirements.

