# Oneflow: Update Contact

Updates an existing contact in Oneflow.

```
PUT https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oneflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Oneflow contact ID. |
| `name` | string | no | The contact name. |
| `email` | string | no | The contact email. |
| `companyName` | string | no | The contact company name. |
| `phoneNumber` | string | no | The contact phone number. |
| `notes` | string | no | Notes for the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_name": "Ava Chen",
      "company_registration_number": "string",
      "country_code": "string",
      "created_time": "string",
      "date_of_birth": "string",
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "notes": "string",
      "phone_number": "string",
      "title": "string",
      "updated_time": "string",
      "workspace_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_name` | string |  |
| `company_registration_number` | string |  |
| `country_code` | string |  |
| `created_time` | string |  |
| `date_of_birth` | string |  |
| `email` | string |  |
| `id` | number |  |
| `name` | string |  |
| `notes` | string |  |
| `phone_number` | string |  |
| `title` | string |  |
| `updated_time` | string |  |
| `workspace_id` | number |  |

## Native endpoint

Through the native Oneflow API, this operation is `PUT /contacts/:id` (base URL `https://api.oneflow.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

