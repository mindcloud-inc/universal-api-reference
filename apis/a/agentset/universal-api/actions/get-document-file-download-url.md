# Agentset: Get Document File Download URL

Retrieves a presigned download URL for a source file from Agentset.

```
GET https://connect.mindcloud.co/v1/universal/agentset/latest/actions/get-document-file-download-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agentset `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentset/latest/actions/get-document-file-download-url?connectionId=$CONNECTION_ID&documentId=string&namespaceId=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string",
  "namespaceId": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentset/latest/actions/get-document-file-download-url?${params}`, {
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
| `documentId` | string | yes | The document ID. |
| `namespaceId` | string | yes | The Agentset namespace ID, prefixed with ns_. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "url": "https://example.com"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.url` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Agentset API, this operation is `POST /v1/namespace/:namespaceId/documents/:documentId/file-download-url` (base URL `https://api.agentset.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-file-download-url.md) for the provider-specific parameters and requirements.

