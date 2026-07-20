# xMatters: Create a scheduled message

Creates a scheduled message in your xMatters instance.

```
POST https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-scheduled-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-scheduled-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-scheduled-message', {
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
| `event` | string | no |  |
| `name` | string | no |  |
| `recurrence` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event": {
        "attachments": [
          {
            "count": 1,
            "data": {
              "links": {
                "self": "https://example.com"
              },
              "name": "Ava Chen",
              "path": "string",
              "size": 1
            },
            "total": 1
          }
        ],
        "bypassPhoneIntro": true,
        "created": "2026-05-07T12:00:00.000Z",
        "escalationOverride": true,
        "eventType": "string",
        "expirationInMinutes": 1,
        "floodControl": true,
        "form": {
          "id": "string",
          "links": {
            "self": "https://example.com"
          },
          "name": "Ava Chen"
        },
        "overrideDeviceRestrictions": true,
        "plan": {
          "id": "string",
          "links": {
            "self": "https://example.com"
          },
          "name": "Ava Chen"
        },
        "priority": "string",
        "properties": {
          "myNumberProperty": 1,
          "myTextProperty": {
            "value": "string"
          }
        },
        "recipients": {
          "count": 1,
          "data": [
            {
              "id": "string",
              "links": {
                "self": "https://example.com"
              },
              "recipientType": "string",
              "targetName": "Ava Chen"
            }
          ],
          "total": 1
        },
        "requirePhonePassword": true,
        "responseCountsEnabled": true,
        "status": "string",
        "voicemailOptions": {
          "every": 1,
          "leave": "ava@example.com",
          "retry": 1
        }
      },
      "id": "string",
      "name": "Ava Chen",
      "owner": {
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "links": {
          "self": "https://example.com"
        },
        "recipientType": "string",
        "status": "string",
        "targetName": "Ava Chen"
      },
      "recurrence": {
        "frequency": "string",
        "startTime": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `event.attachments[].count` | number |  |
| `event.attachments[].data.links.self` | string |  |
| `event.attachments[].data.name` | string |  |
| `event.attachments[].data.path` | string |  |
| `event.attachments[].data.size` | number |  |
| `event.attachments[].total` | number |  |
| `event.bypassPhoneIntro` | boolean |  |
| `event.created` | date |  |
| `event.escalationOverride` | boolean |  |
| `event.eventType` | string |  |
| `event.expirationInMinutes` | number |  |
| `event.floodControl` | boolean |  |
| `event.form.id` | string |  |
| `event.form.links.self` | string |  |
| `event.form.name` | string |  |
| `event.overrideDeviceRestrictions` | boolean |  |
| `event.plan.id` | string |  |
| `event.plan.links.self` | string |  |
| `event.plan.name` | string |  |
| `event.priority` | string |  |
| `event.properties.myNumberProperty` | number |  |
| `event.properties.myTextProperty.value` | string |  |
| `event.recipients.count` | number |  |
| `event.recipients.data[].id` | string |  |
| `event.recipients.data[].links.self` | string |  |
| `event.recipients.data[].recipientType` | string |  |
| `event.recipients.data[].targetName` | string |  |
| `event.recipients.total` | number |  |
| `event.requirePhonePassword` | boolean |  |
| `event.responseCountsEnabled` | boolean |  |
| `event.status` | string |  |
| `event.voicemailOptions.every` | number |  |
| `event.voicemailOptions.leave` | string |  |
| `event.voicemailOptions.retry` | number |  |
| `id` | string |  |
| `name` | string |  |
| `owner.firstName` | string |  |
| `owner.id` | string |  |
| `owner.lastName` | string |  |
| `owner.links.self` | string |  |
| `owner.recipientType` | string |  |
| `owner.status` | string |  |
| `owner.targetName` | string |  |
| `recurrence.frequency` | string |  |
| `recurrence.startTime` | date |  |

## Native endpoint

Through the native xMatters API, this operation is `POST scheduled-messages` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-scheduled-message.md) for the provider-specific parameters and requirements.

