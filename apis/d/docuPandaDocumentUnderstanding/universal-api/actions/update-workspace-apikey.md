# DocuPanda - Document Understanding: Update Workspace Apikey

Updates a workspace API key in DocuPanda.

```
PUT https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/update-workspace-apikey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/update-workspace-apikey" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "newApiKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/update-workspace-apikey', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "newApiKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `newApiKey` | string | yes | New API key for the workspace |
| `workspaceOwnerId` | string | no | Owner ID if admin is updating another user |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": "string",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `message` | string | Response message |
| `name` | string |  |
| `status` | string | Status of the response |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `POST /internal/workspace/update-apikey` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workspace-apikey.md) for the provider-specific parameters and requirements.

