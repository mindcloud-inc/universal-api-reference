# Google AI Studio: Get Batch

Retrieves a batch operation from Google AI Studio.

```
GET https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/get-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google AI Studio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/get-batch?connectionId=$CONNECTION_ID&name=batches%2F1234567890" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "batches/1234567890"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/get-batch?${params}`, {
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
| `name` | string | yes | Full batch resource name, for example `batches/1234567890`. Example: `batches/1234567890`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "done": true,
      "error": {},
      "metadata": {},
      "name": "Ava Chen",
      "response": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `done` | boolean | Whether the operation is complete. |
| `error` | object | Error object when operation failed or was cancelled. |
| `metadata` | object | Service-specific metadata for the operation. |
| `name` | string | Operation resource name. |
| `response` | object | Successful operation response payload. |

## Native endpoint

Through the native Google AI Studio API, this operation is `GET v1beta/batches/:name` (base URL `https://generativelanguage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch.md) for the provider-specific parameters and requirements.

