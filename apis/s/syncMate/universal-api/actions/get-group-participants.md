# SyncMate: Get Group Participants



```
GET https://connect.mindcloud.co/v1/universal/syncMate/latest/actions/get-group-participants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SyncMate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syncMate/latest/actions/get-group-participants?connectionId=$CONNECTION_ID&groupId=120363187342663706%40g.us" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "120363187342663706@g.us"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syncMate/latest/actions/get-group-participants?${params}`, {
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
| `groupId` | string | yes | Full WhatsApp group identifier ending in @g.us. Example: `120363187342663706@g.us`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "status": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `message` | string |  |
| `status` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native SyncMate API, this operation is `GET /api/group/:groupId` (base URL `https://app.assistro.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group-participants.md) for the provider-specific parameters and requirements.

