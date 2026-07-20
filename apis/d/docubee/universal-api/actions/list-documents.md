# Docubee: List Documents

Retrieves documents from Docubee.

```
GET https://connect.mindcloud.co/v1/universal/docubee/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docubee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docubee/latest/actions/list-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docubee/latest/actions/list-documents?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": "string",
      "documentId": "string",
      "name": "Ava Chen",
      "status": "string",
      "tenantId": "string",
      "updatedOn": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | string | When the document was created. |
| `documentId` | string | The Docubee document ID. |
| `name` | string | The document name. |
| `status` | string | The document status. |
| `tenantId` | string | The Docubee tenant ID. |
| `updatedOn` | string | When the document was last updated. |

## Native endpoint

Through the native Docubee API, this operation is `GET /documents` (base URL `https://docubee.app/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

