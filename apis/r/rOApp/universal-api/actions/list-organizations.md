# RO App: List Organizations



```
GET https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RO App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/list-organizations?${params}`, {
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
| `page` | number | no | Page number |
| `names[]` | array<string> | no | List of names |
| `phones[]` | array<string> | no | List of phones |
| `managers[]` | array<number> | no | List of Employee IDs |
| `createdAt[]` | array<date> | no | Filter by creation date. Accepts an array with one or two ISO 8601 date-time values. If one value is provided, it represents the start (left) boundary. If two values are provided, they define a date range (start and end). Examples: ["2025-05-01T00:00:00Z"] — filter from May 1, 2025 onward. ["2025-05-01T00:00:00Z", "2025-05-02T00:00:00Z"] — filter between May 1 and May 2, 2025. |
| `modifiedAt[]` | array<date> | no | Filter by modification date. Accepts an array with one or two ISO 8601 date-time values. If one value is provided, it represents the start (left) boundary. If two values are provided, they define a date range (start and end). Examples: ["2025-05-01T00:00:00Z"] — filter from May 1, 2025 onward. ["2025-05-01T00:00:00Z", "2025-05-02T00:00:00Z"] — filter between May 1 and May 2, 2025. |
| `sort` | string | no | Defines the sorting order of returned results. Use a field name to sort ascending or prefix it with a minus sign (-) to sort descending. |

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

Through the native RO App API, this operation is `GET /contacts/organizations` (base URL `https://api.roapp.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

