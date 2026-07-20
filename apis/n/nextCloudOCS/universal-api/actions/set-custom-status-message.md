# Next Cloud OCS: Set Custom Status Message

Sets custom status message in Next Cloud OCS.

```
PUT https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/set-custom-status-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Next Cloud OCS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/set-custom-status-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/set-custom-status-message', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message` | string | yes | Custom status message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "icon": "string",
      "message": "string",
      "status": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `icon` | string |  |
| `message` | string |  |
| `status` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Next Cloud OCS API, this operation is `PUT /ocs/v2.php/apps/user_status/api/v1/user_status/message/custom` (base URL `https://demo2.nextcloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-custom-status-message.md) for the provider-specific parameters and requirements.

