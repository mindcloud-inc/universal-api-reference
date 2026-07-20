# Pipeline CRM: Update Person

Updates an existing person in Pipeline CRM.

```
PUT https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/update-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipeline CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/update-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/update-person', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deliverReassignmentEmail` | boolean | no | Send an assignment email when the person owner changes. Default: `true`. |
| `id` | number | yes | Person ID |
| `person.firstName` | string | no | The person's first name. |
| `person.lastName` | string | no | The person's last name. |
| `person.fullName` | string | no | The person's full name. |
| `person.summary` | string | no | Summary or notes on the person. |
| `person.phone` | string | no | Person's primary phone number. |
| `person.mobile` | string | no | Person's mobile phone number. |
| `person.position` | string | no | Person's professional position. |
| `person.website` | string | no | Person's website URL. |
| `person.email` | string | no | Person's primary email address. |
| `person.companyId` | number | no | The company ID associated with this person. |
| `person.companyName` | string | no | Associates a company to this person by name, creating it if needed. |
| `person.userId` | number | no | The user ID who owns this person record. |
| `person.leadStatusId` | number | no | The lead status ID to set for this person. |
| `person.leadSourceId` | number | no | The lead source ID to set for this person. |
| `person.predefinedContactsTagIds[]` | array<number> | no | Tag IDs to set on this person. |
| `person.relationship` | string | no | The relationship of the person to the company. |
| `person.isKeyContact` | boolean | no | Whether this person is a key contact for the company. |
| `todoTemplateId` | number | no | The todo template ID to apply to this person. |
| `todoTemplateUserId` | number | no | The owner of tasks created from the todo template. |

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

Through the native Pipeline CRM API, this operation is `PUT /people/:id` (base URL `https://api.pipelinecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-person.md) for the provider-specific parameters and requirements.

