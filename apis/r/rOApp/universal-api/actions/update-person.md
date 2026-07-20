# RO App: Update Person



```
PUT https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/update-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RO App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/update-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "personId": 1,
  "birthday.day": 1,
  "birthday.month": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/update-person', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "personId": 1,
    "birthday.day": 1,
    "birthday.month": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `personId` | number | yes | Person ID |
| `firstName` | string | no | Person first name |
| `lastName` | string | no | Person last name |
| `birthday` | object | no | Person birthday |
| `birthday.day` | number | yes |  |
| `birthday.month` | number | yes |  |
| `birthday.year` | number | no |  |
| `email` | string | no | Valid email |
| `phones[]` | array<object> | no | List of phone numbers |
| `notes` | string | no | Notes text |
| `address` | string | no | Person address |
| `supplier` | boolean | no | Is this person your supplier? |
| `managerId` | number | no | Employee ID |
| `adCampaignId` | number | no | Ad Campaign ID |
| `discountCode` | string | no | Discount code |
| `customFields` | string | no | Custom fields values in format {"f123": "value", "f234": "value"}, where "f123" and "f234" is a custom field id. |
| `tags[]` | array<string> | no | Array of tags |
| `taxIdentificationNumber` | string | no | Tax identification number |

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

Through the native RO App API, this operation is `PATCH /contacts/people/:person_id` (base URL `https://api.roapp.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-person.md) for the provider-specific parameters and requirements.

