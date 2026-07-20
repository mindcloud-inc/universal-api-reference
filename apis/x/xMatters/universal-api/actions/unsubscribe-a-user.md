# xMatters: Unsubscribe a user

Unsubscribes a user from your xMatters instance.

```
DELETE https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/unsubscribe-a-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/unsubscribe-a-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/unsubscribe-a-user?${params}`, {
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
| `subscriberId` | string | no |  |
| `subscriptionId` | string | no |  |

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
| `criteria.data[].value` | string |  |
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
| `targetDeviceNames.count` | number |  |
| `targetDeviceNames.data[].description` | string |  |
| `targetDeviceNames.data[].deviceType` | string |  |
| `targetDeviceNames.data[].name` | string |  |
| `targetDeviceNames.total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `DELETE subscriptions/{subscriptionId}/subscribers/{subscriberId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unsubscribe-a-user.md) for the provider-specific parameters and requirements.

