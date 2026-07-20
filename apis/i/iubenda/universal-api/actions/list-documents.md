# iubenda: List Documents

Retrieves documents from iubenda.

```
GET https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iubenda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/list-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/list-documents?${params}`, {
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
| `limit` | number | no | Maximum number of documents to return. Example: `25`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startingAfterIdentifier` | string | no | Cursor indicating after which identifier document results should be returned. Example: `privacy_policy_v1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "mime_type": "string",
      "name": "Ava Chen",
      "referenced": true,
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Unique document identifier. |
| `mime_type` | string | Document MIME type. |
| `name` | string | Document file name. |
| `referenced` | boolean | Whether the document is referenced by a legal notice or consent. |
| `timestamp` | string | Document upload timestamp. |

## Native endpoint

Through the native iubenda API, this operation is `GET /beta/documents` (base URL `https://consent.iubenda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

