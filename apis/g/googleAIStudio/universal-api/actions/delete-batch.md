# Google AI Studio: Delete Batch

Deletes a batch operation from Google AI Studio.

```
DELETE https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/delete-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google AI Studio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/delete-batch?connectionId=$CONNECTION_ID&name=batches%2F1234567890" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "batches/1234567890"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/delete-batch?${params}`, {
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
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | object | Empty object returned by Gemini when a batch is deleted successfully. |

## Native endpoint

Through the native Google AI Studio API, this operation is `DELETE v1beta/batches/:name` (base URL `https://generativelanguage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-batch.md) for the provider-specific parameters and requirements.

