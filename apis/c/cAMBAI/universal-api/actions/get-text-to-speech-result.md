# CAMB.AI: Get Text-to-Speech Result

Retrieves a text-to-speech result from CAMB.AI.

```
GET https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/get-text-to-speech-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CAMB.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/get-text-to-speech-result?connectionId=$CONNECTION_ID&run_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "run_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/get-text-to-speech-result?${params}`, {
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
| `run_id` | number | yes | Run identifier returned by a completed text-to-speech task. |
| `output_type` | string | no | Response mode for the result; use file_url for a downloadable URL. Default: `file_url`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "output_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `output_url` | string | Download URL when requesting the text-to-speech result as a file URL. |

## Native endpoint

Through the native CAMB.AI API, this operation is `GET /tts-result/:run_id` (base URL `https://client.camb.ai/apis`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-text-to-speech-result.md) for the provider-specific parameters and requirements.

