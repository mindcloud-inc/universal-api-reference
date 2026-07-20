# Contacts+: Create Contact

Creates a new contact in Contacts+.

```
POST https://connect.mindcloud.co/v1/universal/contacts/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Contacts+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/contacts/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contacts/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contact` | object | yes | The contact object to create. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | no | Create the contact in this team instead of personal contacts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {
        "contactData": {
          "emails": [
            {
              "type": "ava@example.com",
              "value": "ava@example.com"
            }
          ],
          "name": {
            "familyName": "Ava Chen",
            "givenName": "Ava Chen"
          }
        },
        "contactId": "string",
        "created": "2026-05-07T12:00:00.000Z",
        "etag": "string",
        "updated": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact.contactData.emails[].type` | string |  |
| `contact.contactData.emails[].value` | string |  |
| `contact.contactData.name.familyName` | string |  |
| `contact.contactData.name.givenName` | string |  |
| `contact.contactId` | string |  |
| `contact.created` | date |  |
| `contact.etag` | string |  |
| `contact.updated` | date |  |

## Native endpoint

Through the native Contacts+ API, this operation is `POST /api/v1/contacts.create` (base URL `https://api.contactsplus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

