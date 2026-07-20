# Zoho Writer: Create/Upload Documents

Creates or uploads a document in Zoho Writer.

```
POST https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/create-upload-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Writer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/create-upload-documents" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/create-upload-documents', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filename` | string | no | Name for the new Writer document. |
| `resourceType` | string | no | Optional document type to create: fillable, merge, or sign. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "title": "string",
      "type": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |
| `title` | string |  |
| `type` | string |  |
| `version` | number |  |

## Native endpoint

Through the native Zoho Writer API, this operation is `POST /v1/documents` (base URL `{{credentials.accessTokenRequest.api_domain}}/writer/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-upload-documents.md) for the provider-specific parameters and requirements.

