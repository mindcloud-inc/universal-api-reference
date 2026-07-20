# xMatters: Get user delivery data

Retrieves user delivery data from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-user-delivery-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-user-delivery-data?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-user-delivery-data?${params}`, {
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
| `at` | string | no |  |
| `embed` | string | no |  |
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
          "deliveryStatus": "string",
          "event": {
            "eventId": "string",
            "id": "string",
            "links": {
              "self": "https://example.com"
            }
          },
          "notifications": {
            "count": 1,
            "data": [
              {
                "category": "string",
                "delivered": "2026-05-07T12:00:00.000Z",
                "deliveryAttempted": "2026-05-07T12:00:00.000Z",
                "deliveryStatus": "string",
                "id": "string",
                "recipient": {
                  "deviceType": "string",
                  "id": "string",
                  "links": {
                    "self": "https://example.com"
                  },
                  "name": "Ava Chen",
                  "recipientType": "string",
                  "targetName": "Ava Chen"
                },
                "responded": "2026-05-07T12:00:00.000Z",
                "responses": {
                  "count": 1,
                  "data": [
                    {
                      "notification": {
                        "id": "string"
                      },
                      "received": "2026-05-07T12:00:00.000Z",
                      "text": "string"
                    }
                  ],
                  "total": 1
                }
              }
            ],
            "total": 1
          },
          "person": {
            "firstName": "Ava",
            "id": "string",
            "lastName": "Chen",
            "links": {
              "self": "https://example.com"
            },
            "properties": {
              "firstAidLevel": [
                [
                  "string"
                ]
              ],
              "isCPR": [
                [
                  "string"
                ]
              ],
              "isFirstAid": [
                [
                  "string"
                ]
              ],
              "location": [
                [
                  "string"
                ]
              ]
            },
            "recipientType": "string",
            "site": {
              "id": "string",
              "links": {
                "self": "https://example.com"
              },
              "name": "Ava Chen"
            },
            "targetName": "Ava Chen"
          },
          "response": {
            "notification": {
              "id": "string"
            },
            "received": "2026-05-07T12:00:00.000Z",
            "text": "string"
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
| `data[].deliveryStatus` | string |  |
| `data[].event.eventId` | string |  |
| `data[].event.id` | string |  |
| `data[].event.links.self` | string |  |
| `data[].notifications.count` | number |  |
| `data[].notifications.data[].category` | string |  |
| `data[].notifications.data[].delivered` | date |  |
| `data[].notifications.data[].deliveryAttempted` | date |  |
| `data[].notifications.data[].deliveryStatus` | string |  |
| `data[].notifications.data[].id` | string |  |
| `data[].notifications.data[].recipient.deviceType` | string |  |
| `data[].notifications.data[].recipient.id` | string |  |
| `data[].notifications.data[].recipient.links.self` | string |  |
| `data[].notifications.data[].recipient.name` | string |  |
| `data[].notifications.data[].recipient.recipientType` | string |  |
| `data[].notifications.data[].recipient.targetName` | string |  |
| `data[].notifications.data[].responded` | date |  |
| `data[].notifications.data[].responses.count` | number |  |
| `data[].notifications.data[].responses.data[].notification.id` | string |  |
| `data[].notifications.data[].responses.data[].received` | date |  |
| `data[].notifications.data[].responses.data[].text` | string |  |
| `data[].notifications.data[].responses.total` | number |  |
| `data[].notifications.total` | number |  |
| `data[].person.firstName` | string |  |
| `data[].person.id` | string |  |
| `data[].person.lastName` | string |  |
| `data[].person.links.self` | string |  |
| `data[].person.properties.firstAidLevel[]` | array<string> |  |
| `data[].person.properties.isCPR[]` | array<string> |  |
| `data[].person.properties.isFirstAid[]` | array<string> |  |
| `data[].person.properties.location[]` | array<string> |  |
| `data[].person.recipientType` | string |  |
| `data[].person.site.id` | string |  |
| `data[].person.site.links.self` | string |  |
| `data[].person.site.name` | string |  |
| `data[].person.targetName` | string |  |
| `data[].response.notification.id` | string |  |
| `data[].response.received` | date |  |
| `data[].response.text` | string |  |
| `links.self` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET events/{eventId}/user-deliveries` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-user-delivery-data.md) for the provider-specific parameters and requirements.

