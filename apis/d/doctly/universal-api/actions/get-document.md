# Doctly: Get Document



```
GET https://connect.mindcloud.co/v1/universal/doctly/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doctly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/doctly/latest/actions/get-document?connectionId=$CONNECTION_ID&id=98287766-3c8f-4407-9df7-f8c702d046df" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "98287766-3c8f-4407-9df7-f8c702d046df"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/doctly/latest/actions/get-document?${params}`, {
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
| `id` | string | yes | Unique document UUID to retrieve. Example: `98287766-3c8f-4407-9df7-f8c702d046df`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accuracy": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "extractorId": "string",
      "fileName": "Ava Chen",
      "fileSize": 1,
      "fileUrl": "https://example.com",
      "id": "string",
      "outputFileName": "Ava Chen",
      "outputFileUrl": "https://example.com",
      "pageCount": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accuracy` | string |  |
| `createdAt` | date |  |
| `extractorId` | string |  |
| `fileName` | string |  |
| `fileSize` | number |  |
| `fileUrl` | string |  |
| `id` | string |  |
| `outputFileName` | string |  |
| `outputFileUrl` | string |  |
| `pageCount` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Doctly API, this operation is `GET /documents/:id` (base URL `https://api.doctly.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

