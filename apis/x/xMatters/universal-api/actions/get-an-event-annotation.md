# xMatters: Get an event annotation

Retrieves an event annotation from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-an-event-annotation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-an-event-annotation?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-an-event-annotation?${params}`, {
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
| `annotationId` | string | no |  |
| `eventId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": {
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "links": {
          "self": "https://example.com"
        },
        "recipientType": "string",
        "targetName": "Ava Chen"
      },
      "comment": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "event": {
        "eventId": "string",
        "id": "string",
        "links": {
          "self": "https://example.com"
        }
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author.firstName` | string |  |
| `author.id` | string |  |
| `author.lastName` | string |  |
| `author.links.self` | string |  |
| `author.recipientType` | string |  |
| `author.targetName` | string |  |
| `comment` | string |  |
| `created` | date |  |
| `event.eventId` | string |  |
| `event.id` | string |  |
| `event.links.self` | string |  |
| `id` | string |  |
| `links.self` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `GET events/{eventId}/annotations/{annotationId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-an-event-annotation.md) for the provider-specific parameters and requirements.

