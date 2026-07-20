# Uku: Create Contact

Creates a new contact in Uku.

```
POST https://connect.mindcloud.co/v1/universal/uku/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uku `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uku/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": "string",
  "email": "ava@example.com",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uku/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": "string",
    "email": "ava@example.com",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | string | yes | Uku client ID |
| `email` | string | yes | Contact email |
| `name` | string | yes | Contact name |

## Response

```json
{
  "success": true,
  "data": [
    {
      "birthday": "string",
      "client_id": 1,
      "created_at": "string",
      "email": "ava@example.com",
      "ext_contact_id": "string",
      "id": 1,
      "is_primary": 1,
      "job_title": "string",
      "mobile_phone": "string",
      "name": "Ava Chen",
      "surname": "Ava Chen",
      "updated_at": "string",
      "work_phone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `birthday` | string |  |
| `client_id` | number |  |
| `created_at` | string |  |
| `email` | string |  |
| `ext_contact_id` | string |  |
| `id` | number |  |
| `is_primary` | number |  |
| `job_title` | string |  |
| `mobile_phone` | string |  |
| `name` | string |  |
| `surname` | string |  |
| `updated_at` | string |  |
| `work_phone` | string |  |

## Native endpoint

Through the native Uku API, this operation is `POST /contacts` (base URL `https://app.getuku.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

