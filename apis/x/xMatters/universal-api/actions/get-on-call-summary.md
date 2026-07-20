# xMatters: Get on-call summary

Retrieves on-call summary from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-on-call-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-on-call-summary?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-on-call-summary?${params}`, {
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
| `groups` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {
          "delay": 1,
          "end": "2026-05-07T12:00:00.000Z",
          "escalationLevel": 1,
          "group": {
            "id": "string",
            "links": {
              "self": "https://example.com"
            },
            "name": "Ava Chen",
            "targetName": "Ava Chen"
          },
          "members": {
            "count": 1,
            "data": [
              {
                "delay": 1,
                "escalationType": "string",
                "member": {
                  "externallyOwned": true,
                  "firstName": "Ava",
                  "id": "string",
                  "language": "string",
                  "lastName": "Chen",
                  "links": {
                    "self": "https://example.com"
                  },
                  "recipientType": "string",
                  "site": {
                    "id": "string",
                    "links": {
                      "self": "https://example.com"
                    }
                  },
                  "status": "string",
                  "targetName": "Ava Chen",
                  "timezone": "string",
                  "webLogin": "string"
                },
                "position": 1,
                "replacements": {
                  "count": 1,
                  "data": [
                    {
                      "end": "2026-05-07T12:00:00.000Z",
                      "replacement": {
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
                      "start": "2026-05-07T12:00:00.000Z"
                    }
                  ],
                  "total": 1
                }
              }
            ],
            "links": {
              "self": "https://example.com"
            },
            "total": 1
          },
          "notifyEndOfEscalation": {
            "notifyEnabled": true
          },
          "occurrenceType": "string",
          "recipient": {
            "displayName": "Ava Chen",
            "firstName": "Ava",
            "id": "string",
            "lastName": "Chen",
            "recipientType": "string",
            "targetName": "Ava Chen"
          },
          "shift": {
            "id": "string",
            "links": {
              "self": "https://example.com"
            },
            "name": "Ava Chen"
          },
          "start": "2026-05-07T12:00:00.000Z"
        }
      ],
      "links": {
        "next": "https://example.com",
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
| `data[].delay` | number |  |
| `data[].end` | date |  |
| `data[].escalationLevel` | number |  |
| `data[].group.id` | string |  |
| `data[].group.links.self` | string |  |
| `data[].group.name` | string |  |
| `data[].group.targetName` | string |  |
| `data[].members.count` | number |  |
| `data[].members.data[].delay` | number |  |
| `data[].members.data[].escalationType` | string |  |
| `data[].members.data[].member.externallyOwned` | boolean |  |
| `data[].members.data[].member.firstName` | string |  |
| `data[].members.data[].member.id` | string |  |
| `data[].members.data[].member.language` | string |  |
| `data[].members.data[].member.lastName` | string |  |
| `data[].members.data[].member.links.self` | string |  |
| `data[].members.data[].member.recipientType` | string |  |
| `data[].members.data[].member.site.id` | string |  |
| `data[].members.data[].member.site.links.self` | string |  |
| `data[].members.data[].member.status` | string |  |
| `data[].members.data[].member.targetName` | string |  |
| `data[].members.data[].member.timezone` | string |  |
| `data[].members.data[].member.webLogin` | string |  |
| `data[].members.data[].position` | number |  |
| `data[].members.data[].replacements.count` | number |  |
| `data[].members.data[].replacements.data[].end` | date |  |
| `data[].members.data[].replacements.data[].replacement.firstName` | string |  |
| `data[].members.data[].replacements.data[].replacement.id` | string |  |
| `data[].members.data[].replacements.data[].replacement.lastName` | string |  |
| `data[].members.data[].replacements.data[].replacement.links.self` | string |  |
| `data[].members.data[].replacements.data[].replacement.recipientType` | string |  |
| `data[].members.data[].replacements.data[].replacement.status` | string |  |
| `data[].members.data[].replacements.data[].replacement.targetName` | string |  |
| `data[].members.data[].replacements.data[].start` | date |  |
| `data[].members.data[].replacements.total` | number |  |
| `data[].members.links.self` | string |  |
| `data[].members.total` | number |  |
| `data[].notifyEndOfEscalation.notifyEnabled` | boolean |  |
| `data[].occurrenceType` | string |  |
| `data[].recipient.displayName` | string |  |
| `data[].recipient.firstName` | string |  |
| `data[].recipient.id` | string |  |
| `data[].recipient.lastName` | string |  |
| `data[].recipient.recipientType` | string |  |
| `data[].recipient.targetName` | string |  |
| `data[].shift.id` | string |  |
| `data[].shift.links.self` | string |  |
| `data[].shift.name` | string |  |
| `data[].start` | date |  |
| `links.next` | string |  |
| `links.self` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET on-call-summary` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-on-call-summary.md) for the provider-specific parameters and requirements.

