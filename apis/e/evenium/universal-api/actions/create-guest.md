# Evenium: Create Guest

Creates a new guest in Evenium.

```
POST https://connect.mindcloud.co/v1/universal/evenium/latest/actions/create-guest
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evenium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/evenium/latest/actions/create-guest" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/evenium/latest/actions/create-guest', {
  method: 'POST',
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
| `company` | string | no | Guest company. |
| `contactId` | string | no | Invite an existing contact by ID. |
| `email` | string | no | Guest email. |
| `eventId` | string | no | The Evenium event ID. |
| `firstName` | string | no | Guest first name. |
| `gender` | string | no | Guest gender. |
| `lastName` | string | no | Guest last name. |
| `status` | string | no | Guest registration status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": 1,
      "creationDate": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "eventId": 1,
      "fields": [
        {}
      ],
      "firstName": "Ava",
      "guestCode": "string",
      "guestId": 1,
      "lastName": "Chen",
      "lastUpdate": "2026-05-07T12:00:00.000Z",
      "password": "string",
      "personId": 1,
      "postStatus": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | number | Guest contact ID. |
| `creationDate` | date | Guest creation timestamp. |
| `email` | string | Guest email address. |
| `eventId` | number | Parent event ID. |
| `fields` | array<object> | Additional guest fields. |
| `firstName` | string | Guest first name. |
| `guestCode` | string | Guest invitation code. |
| `guestId` | number | Guest registration ID. |
| `lastName` | string | Guest last name. |
| `lastUpdate` | date | Last modification timestamp. |
| `password` | string | Guest access password. |
| `personId` | number | Underlying person ID. |
| `postStatus` | string | Guest post-event status. |
| `status` | string | Guest registration status. |

## Native endpoint

Through the native Evenium API, this operation is `POST /events/:eventId/guests` (base URL `https://evenium.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-guest.md) for the provider-specific parameters and requirements.

