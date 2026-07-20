# Blaze AI: Update Doc Access

Updates an existing document access in Blaze AI.

```
PUT https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/update-doc-access
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blaze AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/update-doc-access" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspace_id": "994619",
  "doc_id": "4981633",
  "id": "78391817",
  "permission": "edit"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/update-doc-access', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspace_id": "994619",
    "doc_id": "4981633",
    "id": "78391817",
    "permission": "edit"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspace_id` | number | yes | Blaze workspace ID. Default: `994619`. |
| `doc_id` | number | yes | Blaze document ID. Default: `4981633`. |
| `id` | number | yes | Blaze access record ID. Default: `78391817`. |
| `permission` | string | yes | Updated access permission. Default: `edit`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "accessorId": 1,
        "accessorType": "string",
        "docId": 1,
        "id": 1,
        "inherited": true,
        "permission": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.accessorId` | number |  |
| `data.accessorType` | string |  |
| `data.docId` | number |  |
| `data.id` | number |  |
| `data.inherited` | boolean |  |
| `data.permission` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Blaze AI API, this operation is `PATCH /api/v1/w/:workspace_id/docs/:doc_id/accesses/:id` (base URL `https://api.blaze.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-doc-access.md) for the provider-specific parameters and requirements.

