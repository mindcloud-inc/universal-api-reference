# Contacts+: Search Contacts

Finds contacts in Contacts+ by search query.

```
GET https://connect.mindcloud.co/v1/universal/contacts/latest/actions/search-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Contacts+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contacts/latest/actions/search-contacts?connectionId=$CONNECTION_ID&searchQuery=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchQuery": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contacts/latest/actions/search-contacts?${params}`, {
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
| `searchQuery` | string | yes | Search text used to match contacts. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `searchCursor` | string | no | Cursor for the next page of search results. |
| `teamId` | string | no | Search contacts in this team instead of personal contacts. |

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
        ]
      },
      "contactId": "string",
      "created": "2026-05-07T12:00:00.000Z",
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
| `contactId` | string |  |
| `created` | date |  |
| `updated` | date |  |

## Native endpoint

Through the native Contacts+ API, this operation is `POST /api/v1/contacts.search` (base URL `https://api.contactsplus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-contacts.md) for the provider-specific parameters and requirements.

