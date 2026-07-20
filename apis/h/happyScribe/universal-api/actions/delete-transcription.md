# HappyScribe: Delete Transcription

Deletes a transcription from HappyScribe.

```
DELETE https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/delete-transcription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HappyScribe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/delete-transcription?connectionId=$CONNECTION_ID&id=a034e65cc0544b31bcd43944e7fbdca3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "a034e65cc0544b31bcd43944e7fbdca3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/delete-transcription?${params}`, {
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
| `id` | string | yes | The transcription identifier. Default: `a034e65cc0544b31bcd43944e7fbdca3`. |
| `permanent` | boolean | no | Set true for irreversible deletion; otherwise the transcription moves to Trash. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string | HappyScribe returns an empty body on successful deletion. |

## Native endpoint

Through the native HappyScribe API, this operation is `DELETE /transcriptions/:id` (base URL `https://www.happyscribe.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-transcription.md) for the provider-specific parameters and requirements.

