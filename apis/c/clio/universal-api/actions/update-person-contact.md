# Clio Manage: Update Person Contact

Updates a person contact in Clio Manage by contact ID.

```
PUT https://connect.mindcloud.co/v1/universal/clio/latest/actions/update-person-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clio Manage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clio/latest/actions/update-person-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clio/latest/actions/update-person-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |
| `data.first_name` | string | no |  |
| `data.last_name` | string | no |  |
| `data.email_addresses[0].address` | string | no | Email address to attach to the contact. |
| `data.email_addresses[0].name` | list | no | Label for the contact email address. One of: `Home`, `Other`, `Work`. |
| `data.email_addresses[0].default_email` | boolean | no | Whether the email should be the default email on the contact. |
| `data.phone_numbers[0].number` | string | no | Phone number to attach to the contact. |
| `data.phone_numbers[0].name` | list | no | Label for the contact phone number. One of: `Fax`, `Home`, `Mobile`, `Other`, `Pager`, `Skype`, `Work`. |
| `data.phone_numbers[0].default_number` | boolean | no | Whether the number should be the default phone number on the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "etag": "string",
      "id": 1,
      "initials": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `etag` | string |  |
| `id` | number |  |
| `initials` | string |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Clio Manage API, this operation is `PATCH /contacts/:id.json` (base URL `https://app.clio.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-person-contact.md) for the provider-specific parameters and requirements.

