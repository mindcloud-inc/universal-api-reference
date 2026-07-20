# Grain: Get Recording Transcript SRT

Retrieves a recording transcript in SRT from Grain.

```
GET https://connect.mindcloud.co/v1/universal/grain/latest/actions/get-recording-transcript-srt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grain/latest/actions/get-recording-transcript-srt?connectionId=$CONNECTION_ID&recording_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recording_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grain/latest/actions/get-recording-transcript-srt?${params}`, {
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
| `recording_id` | list<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `text` | string |  |

## Native endpoint

Through the native Grain API, this operation is `GET /v2/recordings/:recording_id/transcript.srt` (base URL `https://api.grain.com/_/public-api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recording-transcript-srt.md) for the provider-specific parameters and requirements.

