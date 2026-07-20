# Kite Suite: Get notification by user Id



```
GET https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-notification-by-user-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-notification-by-user-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-notification-by-user-id?${params}`, {
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
| `id` | string | no | user Id |
| `limit` | string | no |  |

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

Through the native Kite Suite API, this operation is `GET /api/v1/notification/user/:id?limit=5` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-notification-by-user-id.md) for the provider-specific parameters and requirements.

