# Groq: Retrieve File

Retrieves a file from Groq.

```
GET https://connect.mindcloud.co/v1/universal/groq/latest/actions/retrieve-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Groq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/groq/latest/actions/retrieve-file?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/groq/latest/actions/retrieve-file?${params}`, {
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
| `fileId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bytes": 1,
      "createdAt": 1,
      "filename": "Ava Chen",
      "id": "string",
      "object": "string",
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
| `createdAt` | number |  |
| `filename` | string |  |
| `id` | string |  |
| `object` | string |  |
| `purpose` | string |  |

## Native endpoint

Through the native Groq API, this operation is `GET /openai/v1/files/:file_id` (base URL `https://api.groq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-file.md) for the provider-specific parameters and requirements.

