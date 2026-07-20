# DecisionVault: Get Document

Retrieves a document from DecisionVault by ID.

```
GET https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DecisionVault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/get-document?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/get-document?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "document_id": "string",
      "document_request": {},
      "download_url": "https://example.com",
      "expires_in": 1,
      "filename": "Ava Chen",
      "matter_id": "string",
      "size": 1,
      "uploaded_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `document_id` | string |  |
| `document_request` | object |  |
| `download_url` | string |  |
| `expires_in` | number |  |
| `filename` | string |  |
| `matter_id` | string |  |
| `size` | number |  |
| `uploaded_at` | date |  |

## Native endpoint

Through the native DecisionVault API, this operation is `GET /documents/:document_id` (base URL `https://api.decisionvault.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

