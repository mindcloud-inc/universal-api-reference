# Pipeline CRM: Update Company

Updates an existing company in Pipeline CRM.

```
PUT https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/update-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipeline CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/update-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/update-company', {
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
| `deliverReassignmentEmail` | boolean | no | Send an assignment email when the company owner changes. Default: `true`. |
| `id` | number | yes | Company ID |
| `company.name` | string | no | The name of the company. |
| `company.description` | string | no | Description of the company. |
| `company.email` | string | no | The company email address. |
| `company.web` | string | no | The company's website. |
| `company.phone1` | string | no | Primary business number. |
| `company.phone1Desc` | string | no | Description for the primary business number. |
| `company.ownerId` | number | no | The owner user ID of the company. |
| `company.address1` | string | no | First line of the business address. |
| `company.address2` | string | no | Second line of the business address. |
| `company.city` | string | no | Business address city. |
| `company.state` | string | no | Business address state. |
| `company.postalCode` | string | no | Business address postal code. |
| `company.country` | string | no | Business address country. |
| `company.tagIds[]` | array<number> | no | Tag IDs to set on this company. |
| `todoTemplateId` | number | no | The todo template ID to apply to this company. |
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
      "company_country": "string",
      "country": "string",
      "created_at": "string",
      "custom_fields": {},
      "description": "string",
      "email": "ava@example.com",
      "facebook_url": "https://example.com",
      "fax": "string",
      "id": 1,
      "image_mobile_url": "https://example.com",
      "image_thumb_url": "https://example.com",
      "instant_message": "string",
      "linked_in_url": "https://example.com",
      "name": "Ava Chen",
      "next_task_all_day": true,
      "next_task_due": "2026-05-07T12:00:00.000Z",
      "next_task_id": 1,
      "next_task_name": "Ava Chen",
      "owner_id": 1,
      "owner": {
        "full_name": "Ava Chen",
        "id": 1
      },
      "phone1": "string",
      "phone1_desc": "string",
      "phone2": "string",
      "phone2_desc": "string",
      "phone3": "string",
      "phone3_desc": "string",
      "phone4": "string",
      "phone4_desc": "string",
      "possible_notify_user_ids": [
        [
          "string"
        ]
      ],
      "postal_code": "string",
      "shared_user_ids": [
        [
          1
        ]
      ],
      "state": "string",
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
      "twitter": "string",
      "updated_at": "string",
      "web": "string"
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
| `company_country` | string |  |
| `country` | string |  |
| `created_at` | string |  |
| `custom_fields` | object |  |
| `description` | string |  |
| `email` | string |  |
| `facebook_url` | string |  |
| `fax` | string |  |
| `id` | number |  |
| `image_mobile_url` | string |  |
| `image_thumb_url` | string |  |
| `instant_message` | string |  |
| `linked_in_url` | string |  |
| `name` | string |  |
| `next_task_all_day` | boolean |  |
| `next_task_due` | date |  |
| `next_task_id` | number |  |
| `next_task_name` | string |  |
| `owner_id` | number |  |
| `owner.full_name` | string |  |
| `owner.id` | number |  |
| `phone1` | string |  |
| `phone1_desc` | string |  |
| `phone2` | string |  |
| `phone2_desc` | string |  |
| `phone3` | string |  |
| `phone3_desc` | string |  |
| `phone4` | string |  |
| `phone4_desc` | string |  |
| `possible_notify_user_ids[]` | array<string> |  |
| `postal_code` | string |  |
| `shared_user_ids[]` | array<number> |  |
| `state` | string |  |
| `tag_ids[]` | array<number> |  |
| `tags[].id` | number |  |
| `tags[].name` | string |  |
| `twitter` | string |  |
| `updated_at` | string |  |
| `web` | string |  |

## Native endpoint

Through the native Pipeline CRM API, this operation is `PUT /companies/:id` (base URL `https://api.pipelinecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-company.md) for the provider-specific parameters and requirements.

