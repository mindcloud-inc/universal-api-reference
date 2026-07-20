# Contacts+: Scroll Contacts

Retrieves contacts from Contacts+ using a scroll cursor.

```
GET https://connect.mindcloud.co/v1/universal/contacts/latest/actions/scroll-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Contacts+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contacts/latest/actions/scroll-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contacts/latest/actions/scroll-contacts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `size` | number | no | Maximum number of contacts to return. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scrollCursor` | string | no | Cursor for the next page of contacts. Leave blank for the first page. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
        },
        "phoneNumbers": [
          {
            "type": "string",
            "value": "string"
          }
        ],
        "photos": [
          {
            "type": "string",
            "value": "string"
          }
        ]
      },
      "contactId": "string",
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
| `contactData.emails[].type` | string |  |
| `contactData.emails[].value` | string |  |
| `contactData.name.familyName` | string |  |
| `contactData.name.givenName` | string |  |
| `contactData.phoneNumbers[].type` | string |  |
| `contactData.phoneNumbers[].value` | string |  |
| `contactData.photos[].type` | string |  |
| `contactData.photos[].value` | string |  |
| `contactId` | string |  |
| `created` | date |  |
| `etag` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Contacts+ API, this operation is `POST /api/v1/contacts.scroll` (base URL `https://api.contactsplus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scroll-contacts.md) for the provider-specific parameters and requirements.

