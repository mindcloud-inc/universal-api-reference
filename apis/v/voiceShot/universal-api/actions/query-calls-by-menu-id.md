# VoiceShot: Query Calls By Menu ID

Retrieves calls from VoiceShot by menu ID.

```
GET https://connect.mindcloud.co/v1/universal/voiceShot/latest/actions/query-calls-by-menu-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VoiceShot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voiceShot/latest/actions/query-calls-by-menu-id?connectionId=$CONNECTION_ID&menuId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "menuId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voiceShot/latest/actions/query-calls-by-menu-id?${params}`, {
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

Through the native VoiceShot API, this operation is `POST /ivrapi.asp` (base URL `https://api.voiceshot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-calls-by-menu-id.md) for the provider-specific parameters and requirements.

