# Readwise: Get Reader Document Details

Retrieves detailed document information from Readwise Reader.

```
GET https://connect.mindcloud.co/v1/universal/readwise/latest/actions/get-reader-document-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Readwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/readwise/latest/actions/get-reader-document-details?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/readwise/latest/actions/get-reader-document-details?${params}`, {
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
| `documentId` | string | yes | The ID of the document to get details for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": [
        {}
      ],
      "isError": true,
      "jsonrpc": "string",
      "result": {},
      "structuredContent": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | array<object> |  |
| `isError` | boolean |  |
| `jsonrpc` | string |  |
| `result` | object |  |
| `structuredContent` | object |  |

## Native endpoint

Through the native Readwise API, this operation is `POST https://mcp2.readwise.io/mcp` (base URL `https://readwise.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reader-document-details.md) for the provider-specific parameters and requirements.

