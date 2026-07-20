# Kadoa: Delete Notification Channel



```
DELETE https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/delete-notification-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kadoa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/delete-notification-channel?connectionId=$CONNECTION_ID&channelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/delete-notification-channel?${params}`, {
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
| `channelId` | string | yes | Channel ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "channelId": "string"
      },
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.channelId` | string |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Kadoa API, this operation is `DELETE /v5/notifications/channels/:channelId` (base URL `https://api.kadoa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-notification-channel.md) for the provider-specific parameters and requirements.

