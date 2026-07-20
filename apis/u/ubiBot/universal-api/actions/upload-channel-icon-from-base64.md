# UbiBot: Upload Channel Icon From Base64

Updates a channel icon from a Base64 string in UbiBot.

```
PUT https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/upload-channel-icon-from-base64
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UbiBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/upload-channel-icon-from-base64" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/upload-channel-icon-from-base64', {
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
      "desp": "string",
      "errorCode": "string",
      "result": "string",
      "server_time": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `desp` | string | UbiBot error description when the upload request fails. |
| `errorCode` | string | UbiBot error code when the upload request fails. |
| `result` | string | UbiBot success or error result status. |
| `server_time` | date | UbiBot server timestamp. |

## Native endpoint

Through the native UbiBot API, this operation is `POST /channels/:channelId/device/upload_icon_base64` (base URL `https://webapi.ubibot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-channel-icon-from-base64.md) for the provider-specific parameters and requirements.

