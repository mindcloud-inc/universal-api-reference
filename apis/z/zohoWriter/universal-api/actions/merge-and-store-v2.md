# Zoho Writer: Merge and Store V2

Merges a document and stores it in Zoho Writer.

```
POST https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/merge-and-store-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Writer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/merge-and-store-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string",
  "outputSettings": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/merge-and-store-v2', {
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
| `outputSettings` | string | yes | JSON string for the required output_settings payload, including doc_name and folder_id. |
| `mergeData` | string | no | JSON string for merge_data, for example {"data":[{...}]}. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recordId` | string | no | Alternative to merge_data for supported Zoho CRM, Creator, and Bigin templates. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "records": [
        {
          "email": "ava@example.com",
          "name": "Ava Chen",
          "status": "string"
        }
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `records` | array<object> |  |
| `records[].email` | string |  |
| `records[].name` | string |  |
| `records[].status` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Writer API, this operation is `POST /v2/documents/:document_id/merge/store` (base URL `{{credentials.accessTokenRequest.api_domain}}/writer/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/merge-and-store-v2.md) for the provider-specific parameters and requirements.

