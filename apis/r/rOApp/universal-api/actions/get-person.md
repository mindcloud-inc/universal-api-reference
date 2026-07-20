# RO App: Get Person



```
GET https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/get-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RO App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/get-person?connectionId=$CONNECTION_ID&personId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "personId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/get-person?${params}`, {
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
| `personId` | number | yes | Person ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ad_campaign": "string",
      "ad_campaign_id": 1,
      "address": "string",
      "birthday": {
        "day": 1,
        "month": 1,
        "year": 1
      },
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_fields": {},
      "discount_code": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "last_name": "Chen",
      "manager_id": 1,
      "modified_at": "2026-05-07T12:00:00.000Z",
      "notes": "string",
      "phones": {
        "has_viber": true,
        "has_whatsapp": true,
        "notify": true,
        "phone": "string",
        "title": "string"
      },
      "supplier": true,
      "tags": [
        "string"
      ],
      "tax_identification_number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ad_campaign` | string |  |
| `ad_campaign_id` | number |  |
| `address` | string |  |
| `birthday` | object |  |
| `birthday.day` | number |  |
| `birthday.month` | number |  |
| `birthday.year` | number |  |
| `created_at` | date |  |
| `custom_fields` | object |  |
| `discount_code` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | number |  |
| `last_name` | string |  |
| `manager_id` | number |  |
| `modified_at` | date |  |
| `notes` | string |  |
| `phones` | array<object> |  |
| `phones.has_viber` | boolean |  |
| `phones.has_whatsapp` | boolean |  |
| `phones.notify` | boolean |  |
| `phones.phone` | string |  |
| `phones.title` | string |  |
| `supplier` | boolean |  |
| `tags` | array<string> |  |
| `tax_identification_number` | string |  |

## Native endpoint

Through the native RO App API, this operation is `GET /contacts/people/:person_id` (base URL `https://api.roapp.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person.md) for the provider-specific parameters and requirements.

