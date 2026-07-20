# VoiceShot: Delete Pending Calls

Deletes pending calls from a VoiceShot campaign.

```
DELETE https://connect.mindcloud.co/v1/universal/voiceShot/latest/actions/delete-pending-calls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VoiceShot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/voiceShot/latest/actions/delete-pending-calls?connectionId=$CONNECTION_ID&menuId=string&callIds%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "menuId": "string",
  "callIds[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voiceShot/latest/actions/delete-pending-calls?${params}`, {
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
| `menuId` | string | yes | VoiceShot campaign identifier. |
| `callIds[]` | array<string> | yes | Call identifiers to remove from the pending queue. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "errorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string | VoiceShot response comment or error message. |
| `errorId` | string | VoiceShot response error code. 0 means ok. |

## Native endpoint

Through the native VoiceShot API, this operation is `POST /ivrapi.asp` (base URL `https://api.voiceshot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-pending-calls.md) for the provider-specific parameters and requirements.

