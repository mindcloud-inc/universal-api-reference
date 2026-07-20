# RemOnline: Create Person

Creates a new person in RemOnline.

```
POST https://connect.mindcloud.co/v1/universal/remOnline/latest/actions/create-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RemOnline `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/remOnline/latest/actions/create-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Taylor"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/remOnline/latest/actions/create-person', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Taylor"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes | Person first name. Example: `Taylor`. |
| `lastName` | string | no | Person last name. Example: `Jordan`. |
| `birthday` | object | no | Birthday object. |
| `email` | string | no | Valid email address. Example: `taylor.mindcloud@example.com`. |
| `phones[]` | array<object> | no | Array of phone objects. Accepts multiple values as an array. |
| `notes` | string | no | Notes text. |
| `address` | string | no | Person address. |
| `supplier` | boolean | no | Whether the person is a supplier. Default: `false`. |
| `managerId` | number | no | Manager ID. |
| `adCampaignId` | number | no | Advertising campaign ID. |
| `discountCode` | string | no | Discount code. |
| `customFields` | object | no | Custom fields object. |
| `tags[]` | array<string> | no | Array of tags. Accepts multiple values as an array. |
| `taxIdentificationNumber` | string | no | Tax identification number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_fields": {},
      "discount_code": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "last_name": "Chen",
      "modified_at": "2026-05-07T12:00:00.000Z",
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
| `created_at` | date | Created timestamp. |
| `custom_fields` | object | Custom fields object. |
| `discount_code` | string | Discount code. |
| `email` | string | Email address. |
| `first_name` | string | Person first name. |
| `id` | number | Person ID. |
| `last_name` | string | Person last name. |
| `modified_at` | date | Last modified timestamp. |
| `notes` | string | Notes text. |
| `phones` | array<object> | Phone objects. |
| `supplier` | boolean | Supplier flag. |
| `tags` | array<string> | Tags. |
| `tax_identification_number` | string | Tax identification number. |

## Native endpoint

Through the native RemOnline API, this operation is `POST /v2/contacts/people` (base URL `https://api.roapp.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-person.md) for the provider-specific parameters and requirements.

