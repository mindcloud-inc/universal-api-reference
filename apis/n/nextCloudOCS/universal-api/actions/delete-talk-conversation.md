# Next Cloud OCS: Delete Talk Conversation

Deletes a talk conversation from Next Cloud OCS.

```
DELETE https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/delete-talk-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Next Cloud OCS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/delete-talk-conversation?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/delete-talk-conversation?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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

Through the native Next Cloud OCS API, this operation is `DELETE /ocs/v2.php/apps/spreed/api/v4/room/{{token}}` (base URL `https://demo2.nextcloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-talk-conversation.md) for the provider-specific parameters and requirements.

