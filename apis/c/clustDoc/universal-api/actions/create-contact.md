# ClustDoc: Create Contact



```
POST https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClustDoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "firstname": "Ava",
  "lastname": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "firstname": "Ava",
    "lastname": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Contact email address. |
| `firstname` | string | yes | Contact first name. |
| `lastname` | string | yes | Contact last name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "display_name": "Ava Chen",
      "display_name_full": "Ava Chen",
      "email": "ava@example.com",
      "firstname": "Ava",
      "full_name": "Ava Chen",
      "id": 1,
      "initials": "string",
      "is_secured": true,
      "lastname": "Chen",
      "team_id": 1,
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `display_name` | string |  |
| `display_name_full` | string |  |
| `email` | string |  |
| `firstname` | string |  |
| `full_name` | string |  |
| `id` | number |  |
| `initials` | string |  |
| `is_secured` | boolean |  |
| `lastname` | string |  |
| `team_id` | number |  |
| `updated_at` | string |  |

## Native endpoint

Through the native ClustDoc API, this operation is `POST /contacts` (base URL `https://api.clustdoc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

