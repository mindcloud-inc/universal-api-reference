# xMatters: Create a shift

Creates a shift in your xMatters instance.

```
POST https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-shift
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-shift" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-shift', {
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
| `groupId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "end": "2026-05-07T12:00:00.000Z",
      "group": {
        "id": "string",
        "links": {
          "self": "https://example.com"
        },
        "recipientType": "string",
        "targetName": "Ava Chen"
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "members": [
        {
          "delay": 1,
          "escalationType": "string",
          "inRotation": true,
          "position": 1,
          "recipient": {
            "id": "string",
            "recipientType": "string"
          }
        }
      ],
      "name": "Ava Chen",
      "notifyEndOfEscalation": {
        "delay": "string",
        "notificationType": "string",
        "notifyEnabled": "string",
        "recipient": "string"
      },
      "recurrence": {
        "dayOfWeek": "string",
        "dayOfWeekClassifier": "string",
        "end": {
          "endBy": "string"
        },
        "frequency": "string",
        "months": [
          [
            "string"
          ]
        ],
        "on": "string"
      },
      "repeatEscalation": {
        "delay": "string",
        "escalationType": "string",
        "repeatEnabled": "string",
        "repetitions": "string"
      },
      "start": "2026-05-07T12:00:00.000Z",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `description` | string |  |
| `end` | date |  |
| `group.id` | string |  |
| `group.links.self` | string |  |
| `group.recipientType` | string |  |
| `group.targetName` | string |  |
| `id` | string |  |
| `links.self` | string |  |
| `members[].delay` | number |  |
| `members[].escalationType` | string |  |
| `members[].inRotation` | boolean |  |
| `members[].position` | number |  |
| `members[].recipient.id` | string |  |
| `members[].recipient.recipientType` | string |  |
| `name` | string |  |
| `notifyEndOfEscalation.delay` | string |  |
| `notifyEndOfEscalation.notificationType` | string |  |
| `notifyEndOfEscalation.notifyEnabled` | string |  |
| `notifyEndOfEscalation.recipient` | string |  |
| `recurrence.dayOfWeek` | string |  |
| `recurrence.dayOfWeekClassifier` | string |  |
| `recurrence.end.endBy` | string |  |
| `recurrence.frequency` | string |  |
| `recurrence.months[]` | array<string> |  |
| `recurrence.on` | string |  |
| `repeatEscalation.delay` | string |  |
| `repeatEscalation.escalationType` | string |  |
| `repeatEscalation.repeatEnabled` | string |  |
| `repeatEscalation.repetitions` | string |  |
| `start` | date |  |
| `timezone` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `POST groups/{groupId}/shifts` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-shift.md) for the provider-specific parameters and requirements.

