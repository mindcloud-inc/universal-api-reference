# Docubee: Download Document

Downloads a document from Docubee.

```
GET https://connect.mindcloud.co/v1/universal/docubee/latest/actions/download-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docubee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docubee/latest/actions/download-document?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docubee/latest/actions/download-document?${params}`, {
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
| `documentId` | string | no | The Docubee document ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentId": "string",
      "fileContent": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentId` | string | The Docubee document ID used to retrieve the file. |
| `fileContent` | string | The raw document file content. |

## Native endpoint

Through the native Docubee API, this operation is `GET /documents/:documentId` (base URL `https://docubee.app/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-document.md) for the provider-specific parameters and requirements.

