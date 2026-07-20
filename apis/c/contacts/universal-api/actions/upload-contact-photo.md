# Contacts+: Upload Contact Photo

Uploads a photo for an existing Contacts+ contact.

```
PUT https://connect.mindcloud.co/v1/universal/contacts/latest/actions/upload-contact-photo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Contacts+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/contacts/latest/actions/upload-contact-photo" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact": {},
  "photoFile": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contacts/latest/actions/upload-contact-photo', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact": {},
    "photoFile": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contact` | object | yes | The contact object identifying which contact photo to upload. |
| `photoFile` | file | yes | The image file to upload as the contact photo. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | no | Upload the photo to a team contact instead of personal contacts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {
        "contactData": {
          "name": {
            "familyName": "Ava Chen",
            "givenName": "Ava Chen"
          },
          "photos": [
            {
              "type": "string",
              "value": "https://example.com"
            }
          ]
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
| `contact.contactData.name.familyName` | string |  |
| `contact.contactData.name.givenName` | string |  |
| `contact.contactData.photos[].type` | string |  |
| `contact.contactData.photos[].value` | string |  |
| `contact.contactId` | string |  |
| `contact.created` | date |  |
| `contact.etag` | string |  |
| `contact.updated` | date |  |

## Native endpoint

Through the native Contacts+ API, this operation is `POST /api/v1/contacts.uploadPhoto` (base URL `https://api.contactsplus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-contact-photo.md) for the provider-specific parameters and requirements.

