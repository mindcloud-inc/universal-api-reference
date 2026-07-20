# Blaze AI: Add Doc Access

Creates a document access in Blaze AI.

```
POST https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/add-doc-access
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blaze AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/add-doc-access" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspace_id": "994619",
  "doc_id": "4981633",
  "permission": "edit",
  "accessorType": "Group",
  "accessorId": "994233"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/add-doc-access', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspace_id": "994619",
    "doc_id": "4981633",
    "permission": "edit",
    "accessorType": "Group",
    "accessorId": "994233"
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
| `permission` | string | yes | Access permission. Default: `edit`. |
| `accessorType` | string | yes | Accessor type. Default: `Group`. |
| `accessorId` | number | yes | Accessor record ID. Default: `994233`. |

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

Through the native Blaze AI API, this operation is `POST /api/v1/w/:workspace_id/docs/:doc_id/accesses` (base URL `https://api.blaze.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-doc-access.md) for the provider-specific parameters and requirements.

