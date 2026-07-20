# Contacts+: Manage Contact Tags

Adds or removes tags on Contacts+ contacts.

```
PUT https://connect.mindcloud.co/v1/universal/contacts/latest/actions/manage-contact-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Contacts+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/contacts/latest/actions/manage-contact-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contacts/latest/actions/manage-contact-tags', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactIds[]` | array<string> | yes | The contact IDs whose tags should be changed. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `addTagIds[]` | array<string> | no | Tag IDs to add to the contacts. |
| `removeTagIds[]` | array<string> | no | Tag IDs to remove from the contacts. |
| `teamId` | string | no | Manage tags in this team instead of personal contacts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactData": {
        "name": {
          "familyName": "Ava Chen",
          "givenName": "Ava Chen"
        }
      },
      "contactId": "string",
      "contactMetadata": {
        "tagIds": [
          [
            "string"
          ]
        ]
      },
      "created": "2026-05-07T12:00:00.000Z",
      "etag": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactData.name.familyName` | string |  |
| `contactData.name.givenName` | string |  |
| `contactId` | string |  |
| `contactMetadata.tagIds[]` | array<string> |  |
| `created` | date |  |
| `etag` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Contacts+ API, this operation is `POST /api/v1/contacts.manageTags` (base URL `https://api.contactsplus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/manage-contact-tags.md) for the provider-specific parameters and requirements.

