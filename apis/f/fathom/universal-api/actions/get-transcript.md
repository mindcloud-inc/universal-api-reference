# Fathom: Get Transcript

Retrieves a transcript from Fathom.

```
GET https://connect.mindcloud.co/v1/universal/fathom/latest/actions/get-transcript
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fathom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fathom/latest/actions/get-transcript?connectionId=$CONNECTION_ID&recordingId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recordingId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fathom/latest/actions/get-transcript?${params}`, {
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
| `recordingId` | number | yes | The Fathom recording ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "transcript": [
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
| `transcript` | array<object> | Transcript entries with speaker, text, and timestamp. |

## Native endpoint

Through the native Fathom API, this operation is `GET /recordings/:recording_id/transcript` (base URL `https://api.fathom.ai/external/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transcript.md) for the provider-specific parameters and requirements.

