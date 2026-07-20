# xMatters: Get event audit information

Retrieves event audit information from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-event-audit-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-event-audit-information?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-event-audit-information?${params}`, {
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
| `auditType` | string | no |  |
| `eventId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {
          "annotation": {
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
            "event": {
              "eventId": "string",
              "id": "string",
              "links": {
                "self": "https://example.com"
              }
            }
          },
          "at": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "orderId": "string",
          "response": {
            "comment": "string",
            "notification": {
              "category": "string",
              "created": "2026-05-07T12:00:00.000Z",
              "deliveryStatus": "string",
              "event": {
                "eventId": "string",
                "id": "string",
                "links": {
                  "self": "https://example.com"
                }
              },
              "id": "string",
              "recipient": {
                "id": "string",
                "links": {
                  "self": "https://example.com"
                },
                "recipientType": "string",
                "targetName": "Ava Chen"
              }
            },
            "option": {
              "action": "string",
              "contribution": "string",
              "description": "string",
              "id": "string",
              "joinConference": true,
              "number": 1,
              "prompt": "string",
              "redirectUrl": "https://example.com",
              "text": "string"
            },
            "received": "2026-05-07T12:00:00.000Z",
            "response": "string",
            "source": "string"
          },
          "type": "string"
        }
      ],
      "links": {
        "self": "https://example.com"
      },
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data[].annotation.author.firstName` | string |  |
| `data[].annotation.author.id` | string |  |
| `data[].annotation.author.lastName` | string |  |
| `data[].annotation.author.links.self` | string |  |
| `data[].annotation.author.recipientType` | string |  |
| `data[].annotation.author.targetName` | string |  |
| `data[].annotation.comment` | string |  |
| `data[].annotation.event.eventId` | string |  |
| `data[].annotation.event.id` | string |  |
| `data[].annotation.event.links.self` | string |  |
| `data[].at` | date |  |
| `data[].id` | string |  |
| `data[].orderId` | string |  |
| `data[].response.comment` | string |  |
| `data[].response.notification.category` | string |  |
| `data[].response.notification.created` | date |  |
| `data[].response.notification.deliveryStatus` | string |  |
| `data[].response.notification.event.eventId` | string |  |
| `data[].response.notification.event.id` | string |  |
| `data[].response.notification.event.links.self` | string |  |
| `data[].response.notification.id` | string |  |
| `data[].response.notification.recipient.id` | string |  |
| `data[].response.notification.recipient.links.self` | string |  |
| `data[].response.notification.recipient.recipientType` | string |  |
| `data[].response.notification.recipient.targetName` | string |  |
| `data[].response.option.action` | string |  |
| `data[].response.option.contribution` | string |  |
| `data[].response.option.description` | string |  |
| `data[].response.option.id` | string |  |
| `data[].response.option.joinConference` | boolean |  |
| `data[].response.option.number` | number |  |
| `data[].response.option.prompt` | string |  |
| `data[].response.option.redirectUrl` | string |  |
| `data[].response.option.text` | string |  |
| `data[].response.received` | date |  |
| `data[].response.response` | string |  |
| `data[].response.source` | string |  |
| `data[].type` | string |  |
| `links.self` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET audits` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-event-audit-information.md) for the provider-specific parameters and requirements.

