# EZ Texting: List Contacts

Retrieves contacts from EZ Texting.

```
GET https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EZ Texting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/list-contacts?${params}`, {
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
| `filters[email][like]` | string | no | Filter contacts by email |
| `filters[firstName][like]` | string | no | Filter contacts by first name |
| `filters[groupName][like]` | string | no | Filter contacts by group name |
| `filters[lastName][like]` | string | no | Filter contacts by last name |
| `filters[optOut][eq]` | string | no | Filter contacts by opt-out state |
| `filters[phoneNumber][like]` | string | no | Filter contacts by phone number Example: `(737) 337-8315`. |
| `filters[source][eq]` | string | no | Filter contacts by source |
| `page` | number | no | Page offset starting at 0 |
| `size` | number | no | Page size |
| `sort` | string | no | Sort field and direction |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "custom1": "string",
      "custom2": "string",
      "custom3": "string",
      "custom4": "string",
      "custom5": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "groups": [
        [
          {}
        ]
      ],
      "lastName": "Chen",
      "note": "string",
      "optOut": true,
      "phoneNumber": "string",
      "source": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "values": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `custom1` | string |  |
| `custom2` | string |  |
| `custom3` | string |  |
| `custom4` | string |  |
| `custom5` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `groups[]` | array<object> |  |
| `groups[].contactsCount` | number |  |
| `groups[].id` | string |  |
| `groups[].name` | string |  |
| `groups[].note` | string |  |
| `lastName` | string |  |
| `note` | string |  |
| `optOut` | boolean |  |
| `phoneNumber` | string |  |
| `source` | string |  |
| `updatedAt` | date |  |
| `values` | object |  |

## Native endpoint

Through the native EZ Texting API, this operation is `GET /contacts` (base URL `https://a.eztexting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

