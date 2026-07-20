# xMatters: Get scheduled messages

Retrieves scheduled messages from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-scheduled-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-scheduled-messages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-scheduled-messages?${params}`, {
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
      "count": 1,
      "data": [
        {
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
              "isTheScheduleChanging": true,
              "messageEn": "string",
              "summaryEn": "string"
            },
            "recipients": {
              "count": 1,
              "data": [
                {
                  "firstName": "Ava",
                  "id": "string",
                  "lastName": "Chen",
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
            "responseOptions": {
              "count": 1,
              "data": [
                {
                  "action": "string",
                  "allowComments": true,
                  "contribution": "string",
                  "description": "string",
                  "id": "string",
                  "joinConference": true,
                  "number": 1,
                  "order": 1,
                  "prompt": "string",
                  "redirectUrl": "https://example.com",
                  "text": "string",
                  "translations": {
                    "count": 1,
                    "data": [
                      {
                        "description": "string",
                        "id": "string",
                        "language": "string",
                        "prompt": "string",
                        "text": "string"
                      }
                    ],
                    "total": 1
                  }
                }
              ],
              "total": 1
            },
            "status": "string",
            "voicemailOptions": {
              "every": 1,
              "leave": "ava@example.com",
              "retry": 1
            }
          },
          "id": "string",
          "links": {
            "self": "https://example.com"
          },
          "name": "Ava Chen",
          "nextFireTime": "2026-05-07T12:00:00.000Z",
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
          "previousFireTime": "2026-05-07T12:00:00.000Z",
          "recurrence": {
            "end": {
              "date": "2026-05-07T12:00:00.000Z",
              "endBy": "string"
            },
            "frequency": "string",
            "onDays": [
              [
                "string"
              ]
            ],
            "startTime": "2026-05-07T12:00:00.000Z"
          }
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
| `data[].event.bypassPhoneIntro` | boolean |  |
| `data[].event.created` | date |  |
| `data[].event.escalationOverride` | boolean |  |
| `data[].event.eventType` | string |  |
| `data[].event.expirationInMinutes` | number |  |
| `data[].event.floodControl` | boolean |  |
| `data[].event.form.id` | string |  |
| `data[].event.form.links.self` | string |  |
| `data[].event.form.name` | string |  |
| `data[].event.overrideDeviceRestrictions` | boolean |  |
| `data[].event.plan.id` | string |  |
| `data[].event.plan.links.self` | string |  |
| `data[].event.plan.name` | string |  |
| `data[].event.priority` | string |  |
| `data[].event.properties.haveWorkersBeenNotifiedYet` | boolean |  |
| `data[].event.properties.isTheScheduleChanging` | boolean |  |
| `data[].event.properties.messageEn` | string |  |
| `data[].event.properties.summaryEn` | string |  |
| `data[].event.recipients.count` | number |  |
| `data[].event.recipients.data[].firstName` | string |  |
| `data[].event.recipients.data[].id` | string |  |
| `data[].event.recipients.data[].lastName` | string |  |
| `data[].event.recipients.data[].links.self` | string |  |
| `data[].event.recipients.data[].recipientType` | string |  |
| `data[].event.recipients.data[].targetName` | string |  |
| `data[].event.recipients.total` | number |  |
| `data[].event.requirePhonePassword` | boolean |  |
| `data[].event.responseCountsEnabled` | boolean |  |
| `data[].event.responseOptions.count` | number |  |
| `data[].event.responseOptions.data[].action` | string |  |
| `data[].event.responseOptions.data[].allowComments` | boolean |  |
| `data[].event.responseOptions.data[].contribution` | string |  |
| `data[].event.responseOptions.data[].description` | string |  |
| `data[].event.responseOptions.data[].id` | string |  |
| `data[].event.responseOptions.data[].joinConference` | boolean |  |
| `data[].event.responseOptions.data[].number` | number |  |
| `data[].event.responseOptions.data[].order` | number |  |
| `data[].event.responseOptions.data[].prompt` | string |  |
| `data[].event.responseOptions.data[].redirectUrl` | string |  |
| `data[].event.responseOptions.data[].text` | string |  |
| `data[].event.responseOptions.data[].translations.count` | number |  |
| `data[].event.responseOptions.data[].translations.data[].description` | string |  |
| `data[].event.responseOptions.data[].translations.data[].id` | string |  |
| `data[].event.responseOptions.data[].translations.data[].language` | string |  |
| `data[].event.responseOptions.data[].translations.data[].prompt` | string |  |
| `data[].event.responseOptions.data[].translations.data[].text` | string |  |
| `data[].event.responseOptions.data[].translations.total` | number |  |
| `data[].event.responseOptions.total` | number |  |
| `data[].event.status` | string |  |
| `data[].event.voicemailOptions.every` | number |  |
| `data[].event.voicemailOptions.leave` | string |  |
| `data[].event.voicemailOptions.retry` | number |  |
| `data[].id` | string |  |
| `data[].links.self` | string |  |
| `data[].name` | string |  |
| `data[].nextFireTime` | date |  |
| `data[].owner.firstName` | string |  |
| `data[].owner.id` | string |  |
| `data[].owner.lastName` | string |  |
| `data[].owner.links.self` | string |  |
| `data[].owner.recipientType` | string |  |
| `data[].owner.status` | string |  |
| `data[].owner.targetName` | string |  |
| `data[].previousFireTime` | date |  |
| `data[].recurrence.end.date` | date |  |
| `data[].recurrence.end.endBy` | string |  |
| `data[].recurrence.frequency` | string |  |
| `data[].recurrence.onDays[]` | array<string> |  |
| `data[].recurrence.startTime` | date |  |
| `links.self` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET scheduled-messages` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-scheduled-messages.md) for the provider-specific parameters and requirements.

