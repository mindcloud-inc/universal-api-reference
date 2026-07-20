# EventGeek: Create Contact

Creates a new contact in EventGeek.

```
POST https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EventGeek `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "eventgeek-delete-contact-disposable-20260421-1620@mindcloud.co",
  "first_name": "MindCloud",
  "last_name": "Delete Contact Disposable"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "eventgeek-delete-contact-disposable-20260421-1620@mindcloud.co",
    "first_name": "MindCloud",
    "last_name": "Delete Contact Disposable"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Contact email address. Default: `eventgeek-delete-contact-disposable-20260421-1620@mindcloud.co`. |
| `first_name` | string | yes | Contact first name. Default: `MindCloud`. |
| `last_name` | string | yes | Contact last name. Default: `Delete Contact Disposable`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "custom_fields": {},
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `custom_fields` | object |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | string |  |
| `last_name` | string |  |
| `title` | string |  |

## Native endpoint

Through the native EventGeek API, this operation is `POST /contacts` (base URL `https://app.circa.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

