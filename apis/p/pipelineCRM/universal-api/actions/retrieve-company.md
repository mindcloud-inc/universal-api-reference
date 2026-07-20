# Pipeline CRM: Retrieve Company

Retrieves a company from Pipeline CRM.

```
GET https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/retrieve-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipeline CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/retrieve-company?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/retrieve-company?${params}`, {
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
| `id` | number | yes | Company ID |

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

Through the native Pipeline CRM API, this operation is `GET /companies/:id` (base URL `https://api.pipelinecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-company.md) for the provider-specific parameters and requirements.

