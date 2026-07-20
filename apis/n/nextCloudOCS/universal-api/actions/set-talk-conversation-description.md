# Next Cloud OCS: Set Talk Conversation Description

Sets a talk conversation description in Next Cloud OCS.

```
PUT https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/set-talk-conversation-description
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Next Cloud OCS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/set-talk-conversation-description" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/set-talk-conversation-description', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "displayName": "Ava Chen",
      "id": "string",
      "message": "string",
      "name": "Ava Chen",
      "ocs": {},
      "status": "string",
      "statuscode": 1,
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `displayName` | string |  |
| `id` | string |  |
| `message` | string |  |
| `name` | string |  |
| `ocs` | object |  |
| `status` | string |  |
| `statuscode` | number |  |
| `token` | string |  |

## Native endpoint

Through the native Next Cloud OCS API, this operation is `PUT /ocs/v2.php/apps/spreed/api/v4/room/{{token}}/description` (base URL `https://demo2.nextcloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-talk-conversation-description.md) for the provider-specific parameters and requirements.

