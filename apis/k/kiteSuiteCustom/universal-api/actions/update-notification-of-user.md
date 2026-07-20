# Kite Suite: Update notification of user



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-notification-of-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-notification-of-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "isSeen": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-notification-of-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "isSeen": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `id` | string | no | Notification Id |
| `isSeen` | boolean | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "entity": {},
      "message": "string",
      "notificationType": "string",
      "recipients": [
        "string"
      ],
      "sender": "string",
      "subMessage": "string",
      "tagged": [
        "string"
      ],
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | ID of the notification |
| `entity` | object | details of url and icon |
| `message` | string | message |
| `notificationType` | string | type of notification |
| `recipients` | array | array of object {user:"dsjkfsdklf",isSeen:false} |
| `sender` | string | sender id |
| `subMessage` | string | sub message |
| `tagged` | array | array of object {user:"dsjkfsdklf",isSeen:false} |
| `workspace` | string | workspace Id |

## Native endpoint

Through the native Kite Suite API, this operation is `PATCH /api/v1/notification/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-notification-of-user.md) for the provider-specific parameters and requirements.

