# TicketSource: Get Event

Retrieves an event from the TicketSource account.

```
GET https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TicketSource `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/get-event?connectionId=$CONNECTION_ID&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/get-event?${params}`, {
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
| `eventId` | string | yes | The unique identifier for an Event record |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "activated": true,
        "archived": true,
        "category": "string",
        "comment": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "genre": "string",
        "images": [
          {
            "src": "string",
            "type": "string"
          }
        ],
        "keywords": "string",
        "name": "Ava Chen",
        "public": true,
        "reference": "string",
        "terms": "string",
        "thirdPartyConsent": {
          "capture": true,
          "name": "Ava Chen",
          "showConsent": {
            "email": true,
            "post": true,
            "sms": true
          }
        },
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "links": {
        "dates": "https://example.com",
        "self": "https://example.com",
        "venues": "https://example.com"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.activated` | boolean |  |
| `attributes.archived` | boolean |  |
| `attributes.category` | string |  |
| `attributes.comment` | string |  |
| `attributes.createdAt` | date |  |
| `attributes.description` | string |  |
| `attributes.genre` | string |  |
| `attributes.images[].src` | string |  |
| `attributes.images[].type` | string |  |
| `attributes.keywords` | string |  |
| `attributes.name` | string |  |
| `attributes.public` | boolean |  |
| `attributes.reference` | string |  |
| `attributes.terms` | string |  |
| `attributes.thirdPartyConsent.capture` | boolean |  |
| `attributes.thirdPartyConsent.name` | string |  |
| `attributes.thirdPartyConsent.showConsent.email` | boolean |  |
| `attributes.thirdPartyConsent.showConsent.post` | boolean |  |
| `attributes.thirdPartyConsent.showConsent.sms` | boolean |  |
| `attributes.updatedAt` | date |  |
| `id` | string |  |
| `links.dates` | string |  |
| `links.self` | string |  |
| `links.venues` | string |  |
| `type` | string |  |

## Native endpoint

Through the native TicketSource API, this operation is `GET /events/{EventId}` (base URL `https://api.ticketsource.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

