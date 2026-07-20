# VoiceShot: Query Call By Call ID

Retrieves a call from VoiceShot by call ID.

```
GET https://connect.mindcloud.co/v1/universal/voiceShot/latest/actions/query-call-by-call-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VoiceShot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voiceShot/latest/actions/query-call-by-call-id?connectionId=$CONNECTION_ID&menuId=string&callId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "menuId": "string",
  "callId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voiceShot/latest/actions/query-call-by-call-id?${params}`, {
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
| `callId` | string | yes | Call identifier to query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "errorId": "string",
      "menuId": "string",
      "phoneNumbers": [
        {}
      ]
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
| `menuId` | string | VoiceShot campaign identifier returned by the query. |
| `phoneNumbers` | array<object> | Phone-number results returned by VoiceShot. |

## Native endpoint

Through the native VoiceShot API, this operation is `POST /ivrapi.asp` (base URL `https://api.voiceshot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-call-by-call-id.md) for the provider-specific parameters and requirements.

