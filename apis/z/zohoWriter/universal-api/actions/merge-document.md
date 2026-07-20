# Zoho Writer: Merge Document

Merges a document in Zoho Writer.

```
POST https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/merge-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Writer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/merge-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string",
  "outputSettings": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/merge-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string",
    "outputSettings": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes | The unique ID of the Zoho Writer document. |
| `outputSettings` | string | yes | JSON string for the required output_settings payload. At minimum pass the format to generate, for example {"format":"pdf"}. |
| `mergeData` | string | no | JSON string for merge_data, for example {"data":[{...}]}. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recordId` | string | no | Alternative to merge_data for supported Zoho CRM, Creator, and Bigin templates. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho Writer API returns.

## Native endpoint

Through the native Zoho Writer API, this operation is `POST /v1/documents/:document_id/merge` (base URL `{{credentials.accessTokenRequest.api_domain}}/writer/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/merge-document.md) for the provider-specific parameters and requirements.

