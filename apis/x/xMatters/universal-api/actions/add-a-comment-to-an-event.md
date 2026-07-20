# xMatters: Add a comment to an event

Adds a comment to an event in your xMatters instance.

```
POST https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/add-a-comment-to-an-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/add-a-comment-to-an-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/add-a-comment-to-an-event', {
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
| `comment` | string | no |  |
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
      "id": "string"
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

## Native endpoint

Through the native xMatters API, this operation is `POST events/{eventId}/annotations` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-a-comment-to-an-event.md) for the provider-specific parameters and requirements.

