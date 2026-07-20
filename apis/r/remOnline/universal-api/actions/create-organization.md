# RemOnline: Create Organization

Creates a new organization in RemOnline.

```
POST https://connect.mindcloud.co/v1/universal/remOnline/latest/actions/create-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RemOnline `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/remOnline/latest/actions/create-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloud Stage3 Organization"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/remOnline/latest/actions/create-organization', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloud Stage3 Organization"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Organization name. Example: `MindCloud Stage3 Organization`. |
| `email` | string | no | Organization email address. Example: `ops.mindcloud@example.com`. |
| `phones[]` | array<object> | no | Array of phone objects. Accepts multiple values as an array. |
| `notes` | string | no | Notes text. |
| `address` | string | no | Organization address. |
| `supplier` | boolean | no | Whether the organization is a supplier. Default: `false`. |
| `managerId` | number | no | Manager ID. |
| `adCampaignId` | number | no | Advertising campaign ID. |
| `discountCode` | string | no | Discount code. |
| `customFields` | object | no | Custom fields object. |
| `tags[]` | array<string> | no | Array of tags. Accepts multiple values as an array. |
| `taxIdentificationNumber` | string | no | Tax identification number. |
| `businessRegistrationNumber` | string | no | Business registration number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "business_registration_number": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_fields": {},
      "discount_code": "string",
      "email": "ava@example.com",
      "id": 1,
      "modified_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "notes": "string",
      "phones": [
        {}
      ],
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
| `address` | string | Address. |
| `business_registration_number` | string | Business registration number. |
| `created_at` | date | Created timestamp. |
| `custom_fields` | object | Custom fields object. |
| `discount_code` | string | Discount code. |
| `email` | string | Email address. |
| `id` | number | Organization ID. |
| `modified_at` | date | Last modified timestamp. |
| `name` | string | Organization name. |
| `notes` | string | Notes text. |
| `phones` | array<object> | Phone objects. |
| `supplier` | boolean | Supplier flag. |
| `tags` | array<string> | Tags. |
| `tax_identification_number` | string | Tax identification number. |

## Native endpoint

Through the native RemOnline API, this operation is `POST /v2/contacts/organizations` (base URL `https://api.roapp.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-organization.md) for the provider-specific parameters and requirements.

