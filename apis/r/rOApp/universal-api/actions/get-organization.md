# RO App: Get Organization



```
GET https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RO App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/get-organization?connectionId=$CONNECTION_ID&organizationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/get-organization?${params}`, {
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
| `organizationId` | number | yes | Organization ID |

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

Through the native RO App API, this operation is `GET /contacts/organizations/:organization_id` (base URL `https://api.roapp.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

