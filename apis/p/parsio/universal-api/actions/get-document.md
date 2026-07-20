# Parsio: Get Document



```
GET https://connect.mindcloud.co/v1/universal/parsio/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parsio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parsio/latest/actions/get-document?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parsio/latest/actions/get-document?${params}`, {
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
| `documentId` | string | yes | Parsio document ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "credits": 1,
      "filename": "Ava Chen",
      "name": "Ava Chen",
      "processedAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string | Document content type. |
| `createdAt` | date | Document creation timestamp. |
| `credits` | number | Credits consumed. |
| `filename` | string | Stored filename. |
| `name` | string | Document name. |
| `processedAt` | date | Document processing timestamp. |
| `status` | string | Document status. |
| `type` | string | Document type. |

## Native endpoint

Through the native Parsio API, this operation is `GET /docs/:document_id` (base URL `https://api.parsio.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

