# Expiration Reminder: List Contacts

Retrieves contacts from Expiration Reminder.

```
GET https://connect.mindcloud.co/v1/universal/expirationReminder/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Expiration Reminder `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/expirationReminder/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/expirationReminder/latest/actions/list-contacts?${params}`, {
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
| `email` | string | no | Filter contacts by email address. |
| `page` | string | no | Page number to fetch. |
| `sort` | string | no | Field name to sort by. |
| `sortDirection` | string | no | Sort direction. Defaults to asc. |
| `term` | string | no | Filter contacts by a free-text search term. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedTo": {},
      "contactId": "string",
      "customFields": [
        {}
      ],
      "email": "ava@example.com",
      "id": "string",
      "isActive": true,
      "locationId": "string",
      "mobile": "string",
      "modified": "string",
      "name": "Ava Chen",
      "phone": "string",
      "teamId": "string",
      "timezone": "string",
      "typeId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedTo` | object |  |
| `contactId` | string |  |
| `customFields` | array<object> |  |
| `email` | string |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `locationId` | string |  |
| `mobile` | string |  |
| `modified` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `teamId` | string |  |
| `timezone` | string |  |
| `typeId` | string |  |

## Native endpoint

Through the native Expiration Reminder API, this operation is `GET /v1/contacts` (base URL `https://api.expirationreminder.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

