# Deepgram: Get Available Model

Retrieves an available model from Deepgram.

```
GET https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/get-available-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepgram `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/get-available-model?connectionId=$CONNECTION_ID&modelId=Enter%20a%20model%20ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modelId": "Enter a model ID"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/get-available-model?${params}`, {
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
| `modelId` | string | yes | The model UUID or identifier. Example: `Enter a model ID`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "architecture": "string",
      "batch": true,
      "canonicalName": "Ava Chen",
      "formattedOutput": true,
      "languages": [
        "string"
      ],
      "name": "Ava Chen",
      "streaming": true,
      "uuid": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `architecture` | string |  |
| `batch` | boolean |  |
| `canonicalName` | string |  |
| `formattedOutput` | boolean |  |
| `languages` | array<string> |  |
| `name` | string |  |
| `streaming` | boolean |  |
| `uuid` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Deepgram API, this operation is `GET /v1/models/:model_id` (base URL `https://api.deepgram.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-available-model.md) for the provider-specific parameters and requirements.

