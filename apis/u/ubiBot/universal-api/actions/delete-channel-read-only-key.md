# UbiBot: Delete Channel Read-only Key

Deletes a channel read-only key from UbiBot.

```
DELETE https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/delete-channel-read-only-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UbiBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/delete-channel-read-only-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/delete-channel-read-only-key?${params}`, {
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
| `desp` | string | UbiBot error description when the delete request fails. |
| `errorCode` | string | UbiBot error code when the delete request fails. |
| `result` | string | UbiBot success or error result status. |
| `server_time` | date | UbiBot server timestamp. |

## Native endpoint

Through the native UbiBot API, this operation is `POST /channels/:channelId/api_keys` (base URL `https://webapi.ubibot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-channel-read-only-key.md) for the provider-specific parameters and requirements.

