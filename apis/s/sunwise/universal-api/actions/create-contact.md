# Sunwise: Create Contact

Creates or updates a contact in Sunwise.

```
POST https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sunwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "emails": {},
  "telephones": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "emails": {},
    "telephones": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `emails` | object | yes |  |
| `telephones` | object | yes |  |
| `first_lastname` | string | no |  |
| `second_lastname` | string | no |  |
| `integration_source` | string | no |  |
| `status_flag` | string | no | Default: `active`. |
| `agent` | string | no |  |
| `company_name` | string | no |  |
| `contact_origin` | string | no |  |
| `status_contact` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_name": "Ava Chen",
      "created_at": "string",
      "emails": [
        {
          "email": "ava@example.com"
        }
      ],
      "id": "string",
      "name": "Ava Chen",
      "status_contact": "string",
      "status_flag": "string",
      "telephones": [
        {
          "telephone": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_name` | string |  |
| `created_at` | string |  |
| `emails` | array<object> |  |
| `emails[].email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `status_contact` | string |  |
| `status_flag` | string |  |
| `telephones` | array<object> |  |
| `telephones[].telephone` | string |  |

## Native endpoint

Through the native Sunwise API, this operation is `POST /contacts/` (base URL `https://production.sunwise.ai/boty/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

