# Orq.ai: Retrieve File

Retrieves a file from Orq.ai.

```
GET https://connect.mindcloud.co/v1/universal/orqai/latest/actions/retrieve-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orq.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orqai/latest/actions/retrieve-file?connectionId=$CONNECTION_ID&fileId=file_test_id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "file_test_id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orqai/latest/actions/retrieve-file?${params}`, {
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
| `fileId` | string | yes | File ID from the Orq.ai path parameter. Example: `file_test_id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bytes": 1,
      "created": "string",
      "purpose": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bytes` | number |  |
| `created` | string |  |
| `purpose` | string |  |

## Native endpoint

Through the native Orq.ai API, this operation is `GET /v2/files/[:file_id]` (base URL `https://api.orq.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-file.md) for the provider-specific parameters and requirements.

