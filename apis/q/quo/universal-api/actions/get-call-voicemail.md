# Quo: Get Call Voicemail

Retrieves a voicemail for a Quo call.

```
GET https://connect.mindcloud.co/v1/universal/quo/latest/actions/get-call-voicemail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quo/latest/actions/get-call-voicemail?connectionId=$CONNECTION_ID&callId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "callId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quo/latest/actions/get-call-voicemail?${params}`, {
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
| `callId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duration": 1,
      "id": "string",
      "recordingUrl": "https://example.com",
      "status": "string",
      "transcript": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `duration` | number |  |
| `id` | string |  |
| `recordingUrl` | string |  |
| `status` | string |  |
| `transcript` | string |  |

## Native endpoint

Through the native Quo API, this operation is `GET /call-voicemails/:callId` (base URL `https://api.openphone.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call-voicemail.md) for the provider-specific parameters and requirements.

