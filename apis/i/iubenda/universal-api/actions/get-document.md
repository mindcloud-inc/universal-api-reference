# iubenda: Get Document

Retrieves a document from iubenda.

```
GET https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iubenda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/get-document?connectionId=$CONNECTION_ID&documentId=456f1ede-028c-4b96-b0bc-a8d2e85a975c" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "456f1ede-028c-4b96-b0bc-a8d2e85a975c"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/get-document?${params}`, {
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
| `documentId` | string | yes | Unique identifier of the document Example: `456f1ede-028c-4b96-b0bc-a8d2e85a975c`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file_data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file_data` | string | Raw file data returned by the Show Document endpoint. |

## Native endpoint

Through the native iubenda API, this operation is `GET /beta/documents/:id` (base URL `https://consent.iubenda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

