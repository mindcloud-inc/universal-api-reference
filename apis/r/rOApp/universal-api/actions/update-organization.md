# RO App: Update Organization



```
PUT https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/update-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RO App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/update-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/update-organization', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | number | yes | Organization ID |
| `name` | string | no | Organization name |
| `email` | string | no | Organization email |
| `phones[]` | array<object> | no | List of phone numbers |
| `notes` | string | no | Notes text |
| `address` | string | no | Organization address |
| `supplier` | boolean | no | Is this organization your supplier? |
| `managerId` | number | no | Employee ID |
| `adCampaignId` | number | no | Ad Campaign ID |
| `discountCode` | string | no | Discount code |
| `customFields` | string | no | Custom fields values in format {"f123": "value", "f234": "value"}, where "f123" and "f234" is a custom field id. |
| `tags[]` | array<string> | no | Array of tags |
| `taxIdentificationNumber` | string | no | Tax identification number |
| `businessRegistrationNumber` | string | no | Business registration number |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ad_campaign": "string",
      "ad_campaign_id": 1,
      "address": "string",
      "business_registration_number": "string",
      "created_at": [
        "2026-05-07T12:00:00.000Z"
      ],
      "custom_fields": {},
      "discount_code": "string",
      "email": "ava@example.com",
      "id": 1,
      "manager_id": 1,
      "managers": [
        1
      ],
      "modified_at": [
        "2026-05-07T12:00:00.000Z"
      ],
      "name": "Ava Chen",
      "names": [
        "Ava Chen"
      ],
      "notes": "string",
      "page": 1,
      "phones": {
        "has_viber": true,
        "has_whatsapp": true,
        "notify": true,
        "phone": "string",
        "title": "string"
      },
      "sort": "string",
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
| `business_registration_number` | string |  |
| `created_at` | array<date> |  |
| `custom_fields` | object |  |
| `discount_code` | string |  |
| `email` | string |  |
| `id` | number |  |
| `manager_id` | number |  |
| `managers` | array<number> |  |
| `modified_at` | array<date> |  |
| `name` | string |  |
| `names` | array<string> |  |
| `notes` | string |  |
| `page` | number |  |
| `phones` | array<string> |  |
| `phones.has_viber` | boolean |  |
| `phones.has_whatsapp` | boolean |  |
| `phones.notify` | boolean |  |
| `phones.phone` | string |  |
| `phones.title` | string |  |
| `sort` | string |  |
| `supplier` | boolean |  |
| `tags` | array<string> |  |
| `tax_identification_number` | string |  |

## Native endpoint

Through the native RO App API, this operation is `PATCH /contacts/organizations/:organization_id` (base URL `https://api.roapp.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-organization.md) for the provider-specific parameters and requirements.

