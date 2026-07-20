# Mistral AI: List Files

Retrieves available files from Mistral AI.

```
GET https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/list-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mistral AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/list-files?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/list-files?${params}`, {
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
| `includeTotal` | boolean | no | Include the total count in the file list response. |
| `sampleType[]` | array<string> | no | Optional sample type filter list. |
| `source[]` | array<string> | no | Optional source filter list. |
| `search` | string | no | Free-text search filter. |
| `purpose` | string | no | Optional file purpose filter. |
| `mimetypes[]` | array<string> | no | Optional mimetype filter list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "object": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `object` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Mistral AI API, this operation is `GET /v1/files` (base URL `https://api.mistral.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-files.md) for the provider-specific parameters and requirements.

