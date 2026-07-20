# Deepgram: List All Available Models

Retrieves available models from Deepgram.

```
GET https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/list-all-available-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepgram `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/list-all-available-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/list-all-available-models?${params}`, {
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
| `includeOutdated` | boolean | no | Return non-latest versions of models. Example: `Include outdated models`. |

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

Through the native Deepgram API, this operation is `GET /v1/models` (base URL `https://api.deepgram.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-available-models.md) for the provider-specific parameters and requirements.

