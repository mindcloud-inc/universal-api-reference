# Systeme.io: List Contacts

Retrieves the collection of contacts from Systeme.io.

```
GET https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Systeme.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/list-contacts?${params}`, {
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
| `email` | string | no | Filter by exact email. |
| `tags` | string | no | Filter by tag IDs separated by commas. |
| `bounced` | boolean | no | Filter by contact bounced state. |
| `unsubscribed` | boolean | no | Filter by contact unsubscribed state. |
| `needsConfirmation` | boolean | no | Filter by contact needs confirmation state. |
| `registeredBefore` | date | no | Filter contacts registered before a date-time. |
| `registeredAfter` | date | no | Filter contacts registered after a date-time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasMore": true,
      "items": [
        {
          "bounced": true,
          "email": "ava@example.com",
          "id": 1,
          "locale": "string",
          "needsConfirmation": true,
          "registeredAt": "2026-05-07T12:00:00.000Z",
          "unsubscribed": true
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasMore` | boolean | Whether more pages are available. |
| `items` | array<object> | List of contacts. |
| `items[].bounced` | boolean | Bounced state. |
| `items[].email` | string | Contact email. |
| `items[].id` | number | Contact ID. |
| `items[].locale` | string | Contact locale. |
| `items[].needsConfirmation` | boolean | Needs confirmation state. |
| `items[].registeredAt` | date | Contact registration timestamp. |
| `items[].unsubscribed` | boolean | Unsubscribed state. |

## Native endpoint

Through the native Systeme.io API, this operation is `GET /api/contacts` (base URL `https://api.systeme.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

