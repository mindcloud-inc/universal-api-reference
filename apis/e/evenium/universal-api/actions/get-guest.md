# Evenium: Get Guest

Retrieves a guest from Evenium.

```
GET https://connect.mindcloud.co/v1/universal/evenium/latest/actions/get-guest
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evenium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evenium/latest/actions/get-guest?connectionId=$CONNECTION_ID&contactId=1&eventId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "1",
  "eventId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evenium/latest/actions/get-guest?${params}`, {
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
| `contactId` | number | yes | The Evenium Contact ID. |
| `eventId` | number | yes | The Evenium Event ID. |

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

Through the native Evenium API, this operation is `GET /events/:eventId/guests/:contactId` (base URL `https://evenium.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-guest.md) for the provider-specific parameters and requirements.

