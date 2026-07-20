# Docutray: Delete Knowledge Base Document



```
DELETE https://connect.mindcloud.co/v1/universal/docutray/latest/actions/delete-knowledge-base-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docutray `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/docutray/latest/actions/delete-knowledge-base-document?connectionId=$CONNECTION_ID&documentId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docutray/latest/actions/delete-knowledge-base-document?${params}`, {
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
| `documentId` | string | yes | Unique ID of the document |
| `id` | string | yes | Unique ID of the Knowledge Base |

## Response

```json
{
  "success": true,
  "data": [
    {
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `statusCode` | number |  |

## Native endpoint

Through the native Docutray API, this operation is `DELETE api/knowledge-bases/:id/documents/:documentId` (base URL `https://app.docutray.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-knowledge-base-document.md) for the provider-specific parameters and requirements.

