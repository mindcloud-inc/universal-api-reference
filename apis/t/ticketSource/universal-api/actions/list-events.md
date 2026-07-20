# TicketSource: List Events

Retrieves events from the TicketSource account.

```
GET https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TicketSource `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/list-events?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native TicketSource API, this operation is `GET /events` (base URL `https://api.ticketsource.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

