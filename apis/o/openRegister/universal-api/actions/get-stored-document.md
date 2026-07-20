# OpenRegister: Get Stored Document

Retrieves a stored document from OpenRegister by document ID.

```
GET https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/get-stored-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenRegister `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/get-stored-document?connectionId=$CONNECTION_ID&documentId=document_id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "document_id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/get-stored-document?${params}`, {
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
| `documentId` | string | yes | Stored document ID to retrieve. Example: `document_id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Document date. |
| `id` | string | Stored document ID. |
| `name` | string | Document display name. |
| `type` | string | Document type. |
| `url` | string | Download URL for the stored document. |

## Native endpoint

Through the native OpenRegister API, this operation is `GET /v1/document/:document_id` (base URL `https://api.openregister.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stored-document.md) for the provider-specific parameters and requirements.

