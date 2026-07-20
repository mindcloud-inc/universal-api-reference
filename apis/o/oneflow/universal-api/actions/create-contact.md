# Oneflow: Create Contact

Creates a contact in Oneflow.

```
POST https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oneflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | number | yes | The workspace where the contact should be created. |
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

Through the native Oneflow API, this operation is `POST /contacts` (base URL `https://api.oneflow.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

