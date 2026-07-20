# CallScaler: Get Call Transcription

Retrieves a call transcription from CallScaler.

```
GET https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/get-call-transcription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallScaler `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/get-call-transcription?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/get-call-transcription?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "transcription": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `transcription` | string | AI transcription text for the call. |

## Native endpoint

Through the native CallScaler API, this operation is `GET /calls/:id/transcription` (base URL `https://callscaler.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call-transcription.md) for the provider-specific parameters and requirements.

