# Soniox: Delete transcription

Deletes an existing transcription from Soniox.

```
DELETE https://connect.mindcloud.co/v1/universal/soniox/latest/actions/delete-transcription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Soniox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/soniox/latest/actions/delete-transcription?connectionId=$CONNECTION_ID&transcriptionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transcriptionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/soniox/latest/actions/delete-transcription?${params}`, {
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
| `transcriptionId` | string | yes | Unique identifier of the transcription. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Soniox API returns.

## Native endpoint

Through the native Soniox API, this operation is `DELETE /transcriptions/:transcription_id` (base URL `https://api.soniox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-transcription.md) for the provider-specific parameters and requirements.

