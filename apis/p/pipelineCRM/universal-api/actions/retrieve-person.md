# Pipeline CRM: Retrieve Person

Retrieves a person from Pipeline CRM.

```
GET https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/retrieve-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipeline CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/retrieve-person?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/retrieve-person?${params}`, {
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
| `id` | number | yes | Person ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bounced": true,
      "company_id": 1,
      "company_name": "Ava Chen",
      "created_at": "string",
      "custom_fields": {},
      "email": "ava@example.com",
      "email2": "ava@example.com",
      "facebook_url": "https://example.com",
      "first_name": "Ava",
      "full_name": "Ava Chen",
      "home_address_1": "string",
      "home_address_2": "string",
      "home_city": "string",
      "home_country": "string",
      "home_email": "ava@example.com",
      "home_phone": "string",
      "home_postal_code": "string",
      "home_state": "string",
      "id": 1,
      "image_mobile_url": "https://example.com",
      "image_thumb_url": "https://example.com",
      "instant_message": "string",
      "is_key_contact": true,
      "last_emailed_at": "ava@example.com",
      "last_name": "Chen",
      "lead_source_id": 1,
      "lead_source": {
        "id": 1,
        "name": "Ava Chen"
      },
      "lead_status_id": 1,
      "lead_status": {
        "id": 1,
        "name": "Ava Chen"
      },
      "linked_in_url": "https://example.com",
      "mobile": "string",
      "next_task_all_day": true,
      "next_task_due": "2026-05-07T12:00:00.000Z",
      "next_task_id": 1,
      "next_task_name": "Ava Chen",
      "phone": "string",
      "position": "string",
      "possible_notify_user_ids": [
        [
          1
        ]
      ],
      "predefined_contacts_tag_ids": [
        [
          1
        ]
      ],
      "predefined_contacts_tags": [
        {
          "id": 1,
          "name": "Ava Chen"
        }
      ],
      "relationship": "string",
      "shared_user_ids": [
        [
          1
        ]
      ],
      "summary": "string",
      "twitter": "string",
      "unsubscribed": true,
      "updated_at": "string",
      "user_id": 1,
      "user": {
        "full_name": "Ava Chen",
        "id": 1
      },
      "website": "string",
      "work_address_1": "string",
      "work_address_2": "string",
      "work_city": "string",
      "work_country": "string",
      "work_postal_code": "string",
      "work_state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounced` | boolean |  |
| `company_id` | number |  |
| `company_name` | string |  |
| `created_at` | string |  |
| `custom_fields` | object |  |
| `email` | string |  |
| `email2` | string |  |
| `facebook_url` | string |  |
| `first_name` | string |  |
| `full_name` | string |  |
| `home_address_1` | string |  |
| `home_address_2` | string |  |
| `home_city` | string |  |
| `home_country` | string |  |
| `home_email` | string |  |
| `home_phone` | string |  |
| `home_postal_code` | string |  |
| `home_state` | string |  |
| `id` | number |  |
| `image_mobile_url` | string |  |
| `image_thumb_url` | string |  |
| `instant_message` | string |  |
| `is_key_contact` | boolean |  |
| `last_emailed_at` | string |  |
| `last_name` | string |  |
| `lead_source_id` | number |  |
| `lead_source.id` | number |  |
| `lead_source.name` | string |  |
| `lead_status_id` | number |  |
| `lead_status.id` | number |  |
| `lead_status.name` | string |  |
| `linked_in_url` | string |  |
| `mobile` | string |  |
| `next_task_all_day` | boolean |  |
| `next_task_due` | date |  |
| `next_task_id` | number |  |
| `next_task_name` | string |  |
| `phone` | string |  |
| `position` | string |  |
| `possible_notify_user_ids[]` | array<number> |  |
| `predefined_contacts_tag_ids[]` | array<number> |  |
| `predefined_contacts_tags[].id` | number |  |
| `predefined_contacts_tags[].name` | string |  |
| `relationship` | string |  |
| `shared_user_ids[]` | array<number> |  |
| `summary` | string |  |
| `twitter` | string |  |
| `unsubscribed` | boolean |  |
| `updated_at` | string |  |
| `user_id` | number |  |
| `user.full_name` | string |  |
| `user.id` | number |  |
| `website` | string |  |
| `work_address_1` | string |  |
| `work_address_2` | string |  |
| `work_city` | string |  |
| `work_country` | string |  |
| `work_postal_code` | string |  |
| `work_state` | string |  |

## Native endpoint

Through the native Pipeline CRM API, this operation is `GET /people/:id` (base URL `https://api.pipelinecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-person.md) for the provider-specific parameters and requirements.

