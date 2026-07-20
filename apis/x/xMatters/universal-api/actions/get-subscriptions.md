# xMatters: Get subscriptions

Retrieves subscriptions from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-subscriptions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-subscriptions?${params}`, {
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
| `owner` | string | no |  |
| `subscriptionForm` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {
          "created": "2026-05-07T12:00:00.000Z",
          "criteria": {
            "count": 1,
            "data": [
              {
                "name": "Ava Chen",
                "operator": "string",
                "value": "string"
              }
            ],
            "total": 1
          },
          "description": "string",
          "form": {
            "id": "string",
            "links": {
              "self": "https://example.com"
            },
            "name": "Ava Chen",
            "plan": {
              "id": "string",
              "links": {
                "self": "https://example.com"
              },
              "name": "Ava Chen"
            }
          },
          "id": "string",
          "links": {
            "self": "https://example.com"
          },
          "name": "Ava Chen",
          "notificationDelay": 1,
          "owner": {
            "firstName": "Ava",
            "id": "string",
            "lastName": "Chen",
            "links": {
              "self": "https://example.com"
            },
            "recipientType": "string",
            "targetName": "Ava Chen"
          },
          "recipients": {
            "count": 1,
            "data": [
              {
                "externallyOwned": true,
                "firstName": "Ava",
                "id": "string",
                "language": "string",
                "lastLogin": "2026-05-07T12:00:00.000Z",
                "lastName": "Chen",
                "links": {
                  "self": "https://example.com"
                },
                "recipientType": "string",
                "site": {
                  "id": "string",
                  "links": {
                    "self": "https://example.com"
                  },
                  "name": "Ava Chen"
                },
                "status": "string",
                "targeted": true,
                "targetName": "Ava Chen",
                "timezone": "string",
                "webLogin": "string"
              }
            ],
            "links": {
              "self": "https://example.com"
            },
            "total": 1
          },
          "self": "string",
          "targetDeviceNames": {
            "count": 1,
            "data": [
              {
                "description": "Ava Chen",
                "deviceType": "Ava Chen",
                "domains": [
                  [
                    "Ava Chen"
                  ]
                ],
                "name": "Ava Chen"
              }
            ],
            "total": 1
          }
        }
      ],
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
| `data[].created` | date |  |
| `data[].criteria.count` | number |  |
| `data[].criteria.data[].name` | string |  |
| `data[].criteria.data[].operator` | string |  |
| `data[].criteria.data[].value` | string |  |
| `data[].criteria.total` | number |  |
| `data[].description` | string |  |
| `data[].form.id` | string |  |
| `data[].form.links.self` | string |  |
| `data[].form.name` | string |  |
| `data[].form.plan.id` | string |  |
| `data[].form.plan.links.self` | string |  |
| `data[].form.plan.name` | string |  |
| `data[].id` | string |  |
| `data[].links.self` | string |  |
| `data[].name` | string |  |
| `data[].notificationDelay` | number |  |
| `data[].owner.firstName` | string |  |
| `data[].owner.id` | string |  |
| `data[].owner.lastName` | string |  |
| `data[].owner.links.self` | string |  |
| `data[].owner.recipientType` | string |  |
| `data[].owner.targetName` | string |  |
| `data[].recipients.count` | number |  |
| `data[].recipients.data[].externallyOwned` | boolean |  |
| `data[].recipients.data[].firstName` | string |  |
| `data[].recipients.data[].id` | string |  |
| `data[].recipients.data[].language` | string |  |
| `data[].recipients.data[].lastLogin` | date |  |
| `data[].recipients.data[].lastName` | string |  |
| `data[].recipients.data[].links.self` | string |  |
| `data[].recipients.data[].recipientType` | string |  |
| `data[].recipients.data[].site.id` | string |  |
| `data[].recipients.data[].site.links.self` | string |  |
| `data[].recipients.data[].site.name` | string |  |
| `data[].recipients.data[].status` | string |  |
| `data[].recipients.data[].targeted` | boolean |  |
| `data[].recipients.data[].targetName` | string |  |
| `data[].recipients.data[].timezone` | string |  |
| `data[].recipients.data[].webLogin` | string |  |
| `data[].recipients.links.self` | string |  |
| `data[].recipients.total` | number |  |
| `data[].self` | string |  |
| `data[].targetDeviceNames.count` | number |  |
| `data[].targetDeviceNames.data[].description` | string |  |
| `data[].targetDeviceNames.data[].deviceType` | string |  |
| `data[].targetDeviceNames.data[].domains[]` | array<string> |  |
| `data[].targetDeviceNames.data[].name` | string |  |
| `data[].targetDeviceNames.total` | number |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET subscriptions` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-subscriptions.md) for the provider-specific parameters and requirements.

