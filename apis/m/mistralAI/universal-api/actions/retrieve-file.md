# Mistral AI: Retrieve File

Retrieves file details from Mistral AI.

```
GET https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/retrieve-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mistral AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/retrieve-file?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/retrieve-file?${params}`, {
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
| `fileId` | string | yes | The ID of the file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bytes": 1,
      "created_at": 1,
      "deleted": true,
      "expires_at": "string",
      "filename": "Ava Chen",
      "id": "string",
      "mimetype": "string",
      "num_lines": 1,
      "object": "string",
      "purpose": "string",
      "sample_type": "string",
      "signature": "string",
      "source": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bytes` | number |  |
| `created_at` | number |  |
| `deleted` | boolean |  |
| `expires_at` | string |  |
| `filename` | string |  |
| `id` | string |  |
| `mimetype` | string |  |
| `num_lines` | number |  |
| `object` | string |  |
| `purpose` | string |  |
| `sample_type` | string |  |
| `signature` | string |  |
| `source` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Mistral AI API, this operation is `GET /v1/files/:file_id` (base URL `https://api.mistral.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-file.md) for the provider-specific parameters and requirements.

