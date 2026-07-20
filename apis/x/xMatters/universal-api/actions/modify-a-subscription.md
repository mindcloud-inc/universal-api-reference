# xMatters: Modify a subscription

Updates a subscription in your xMatters instance.

```
PUT https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-subscription', {
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
| `id` | string | no |  |
| `targetAllDevices` | boolean | no |  |
| `targetDeviceNames` | list<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "criteria": {
        "count": 1,
        "data": [
          {
            "name": "Ava Chen",
            "operator": "string"
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
            "lastName": "Chen",
            "links": {
              "self": "https://example.com"
            },
            "properties": {
              "checkbox": true,
              "incidentManager": true
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
        "total": 1
      },
      "targetDeviceNames": {
        "count": 1,
        "data": [
          {
            "description": "Ava Chen",
            "deviceType": "Ava Chen",
            "name": "Ava Chen"
          }
        ],
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `criteria.count` | number |  |
| `criteria.data[].name` | string |  |
| `criteria.data[].operator` | string |  |
| `criteria.total` | number |  |
| `description` | string |  |
| `form.id` | string |  |
| `form.links.self` | string |  |
| `form.name` | string |  |
| `form.plan.id` | string |  |
| `form.plan.name` | string |  |
| `id` | string |  |
| `links.self` | string |  |
| `name` | string |  |
| `notificationDelay` | number |  |
| `owner.firstName` | string |  |
| `owner.id` | string |  |
| `owner.lastName` | string |  |
| `owner.links.self` | string |  |
| `owner.recipientType` | string |  |
| `owner.targetName` | string |  |
| `recipients.count` | number |  |
| `recipients.data[].externallyOwned` | boolean |  |
| `recipients.data[].firstName` | string |  |
| `recipients.data[].id` | string |  |
| `recipients.data[].language` | string |  |
| `recipients.data[].lastName` | string |  |
| `recipients.data[].links.self` | string |  |
| `recipients.data[].properties.checkbox` | boolean |  |
| `recipients.data[].properties.incidentManager` | boolean |  |
| `recipients.data[].recipientType` | string |  |
| `recipients.data[].site.id` | string |  |
| `recipients.data[].site.links.self` | string |  |
| `recipients.data[].site.name` | string |  |
| `recipients.data[].status` | string |  |
| `recipients.data[].targeted` | boolean |  |
| `recipients.data[].targetName` | string |  |
| `recipients.data[].timezone` | string |  |
| `recipients.data[].webLogin` | string |  |
| `recipients.total` | number |  |
| `targetDeviceNames.count` | number |  |
| `targetDeviceNames.data[].description` | string |  |
| `targetDeviceNames.data[].deviceType` | string |  |
| `targetDeviceNames.data[].name` | string |  |
| `targetDeviceNames.total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `POST subscriptions` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/modify-a-subscription.md) for the provider-specific parameters and requirements.

