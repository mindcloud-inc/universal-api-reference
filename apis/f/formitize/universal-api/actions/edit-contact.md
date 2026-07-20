# Formitize: Edit Contact

Updates an existing contact in Formitize.

```
PUT https://connect.mindcloud.co/v1/universal/formitize/latest/actions/edit-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formitize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/formitize/latest/actions/edit-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formitize/latest/actions/edit-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | no | Formitize contact ID. |
| `id` | string | no | Formitize client ID for contact update path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "custom": [
        {}
      ],
      "email": "ava@example.com",
      "firstName": "Ava",
      "homePhone": "string",
      "homePhoneAreaCode": "string",
      "id": "string",
      "lastName": "Chen",
      "mobile": "string",
      "mobileAreaCode": "string",
      "workPhone": "string",
      "workPhoneAreaCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `custom` | array<object> |  |
| `email` | string |  |
| `firstName` | string |  |
| `homePhone` | string |  |
| `homePhoneAreaCode` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `mobile` | string |  |
| `mobileAreaCode` | string |  |
| `workPhone` | string |  |
| `workPhoneAreaCode` | string |  |

## Native endpoint

Through the native Formitize API, this operation is `POST /crm/client/:id/contact/:contactID` (base URL `https://service.formitize.com/api/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-contact.md) for the provider-specific parameters and requirements.

