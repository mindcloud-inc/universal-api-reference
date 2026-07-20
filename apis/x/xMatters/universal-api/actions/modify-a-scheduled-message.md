# xMatters: Modify a scheduled message

Updates a scheduled message in your xMatters instance.

```
PUT https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-scheduled-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-scheduled-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-scheduled-message', {
  method: 'PUT',
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
| `id` | string | no |  |
| `name` | string | no |  |
| `recurrence` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": {
        "count": 1,
        "data": [
          {
            "links": {
              "self": "https://example.com"
            },
            "name": "Ava Chen",
            "path": "string",
            "size": 1
          }
        ],
        "total": 1
      },
      "event": {
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
          "haveWorkersBeenNotifiedYet": true,
          "isTheScheduleChanging": true
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
| `attachments.count` | number |  |
| `attachments.data[].links.self` | string |  |
| `attachments.data[].name` | string |  |
| `attachments.data[].path` | string |  |
| `attachments.data[].size` | number |  |
| `attachments.total` | number |  |
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
| `event.properties.haveWorkersBeenNotifiedYet` | boolean |  |
| `event.properties.isTheScheduleChanging` | boolean |  |
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

Through the native xMatters API, this operation is `POST scheduled-messages` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/modify-a-scheduled-message.md) for the provider-specific parameters and requirements.

