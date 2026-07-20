# xMatters: Create a subscription form

Creates a subscription form in your xMatters instance.

```
POST https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-subscription-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-subscription-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-subscription-form', {
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
| `description` | string | no |  |
| `devicesSectionCollapsed` | boolean | no |  |
| `devicesSectionVisible` | boolean | no |  |
| `name` | string | no |  |
| `notificationDelay` | number | no |  |
| `oneWay` | boolean | no |  |
| `planId` | string | no |  |
| `propertyDefinitions` | list<string> | no |  |
| `roles` | list<string> | no |  |
| `scope` | string | no |  |
| `subscribeOthers` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "devicesSectionCollapsed": true,
      "devicesSectionVisible": true,
      "form": {
        "id": "string",
        "name": "Ava Chen"
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "name": "Ava Chen",
      "notificationDelay": 1,
      "oneWay": true,
      "plan": {
        "id": "string",
        "name": "Ava Chen"
      },
      "propertyDefinitions": {
        "count": 1,
        "data": [
          {
            "default": "string",
            "description": "string",
            "helpText": "string",
            "id": "string",
            "items": [
              [
                "string"
              ]
            ],
            "name": "Ava Chen",
            "propertyType": "string"
          }
        ],
        "total": 1
      },
      "roles": {
        "count": 1,
        "data": [
          {
            "description": "string",
            "id": "string",
            "name": "Ava Chen"
          }
        ],
        "total": 1
      },
      "scope": "string",
      "showNotificationDelay": true,
      "subscribeOthers": true,
      "targetDeviceNames": {
        "count": 1,
        "data": [
          {
            "deviceType": "Ava Chen",
            "name": "Ava Chen"
          }
        ],
        "total": 1
      },
      "visibleTargetDeviceNames": {
        "count": 1,
        "data": [
          {
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
| `description` | string |  |
| `devicesSectionCollapsed` | boolean |  |
| `devicesSectionVisible` | boolean |  |
| `form.id` | string |  |
| `form.name` | string |  |
| `id` | string |  |
| `links.self` | string |  |
| `name` | string |  |
| `notificationDelay` | number |  |
| `oneWay` | boolean |  |
| `plan.id` | string |  |
| `plan.name` | string |  |
| `propertyDefinitions.count` | number |  |
| `propertyDefinitions.data[].default` | string |  |
| `propertyDefinitions.data[].description` | string |  |
| `propertyDefinitions.data[].helpText` | string |  |
| `propertyDefinitions.data[].id` | string |  |
| `propertyDefinitions.data[].items[]` | array<string> |  |
| `propertyDefinitions.data[].name` | string |  |
| `propertyDefinitions.data[].propertyType` | string |  |
| `propertyDefinitions.total` | number |  |
| `roles.count` | number |  |
| `roles.data[].description` | string |  |
| `roles.data[].id` | string |  |
| `roles.data[].name` | string |  |
| `roles.total` | number |  |
| `scope` | string |  |
| `showNotificationDelay` | boolean |  |
| `subscribeOthers` | boolean |  |
| `targetDeviceNames.count` | number |  |
| `targetDeviceNames.data[].deviceType` | string |  |
| `targetDeviceNames.data[].name` | string |  |
| `targetDeviceNames.total` | number |  |
| `visibleTargetDeviceNames.count` | number |  |
| `visibleTargetDeviceNames.data[].deviceType` | string |  |
| `visibleTargetDeviceNames.data[].name` | string |  |
| `visibleTargetDeviceNames.total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `POST plans/{planId}/subscription-forms` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-subscription-form.md) for the provider-specific parameters and requirements.

