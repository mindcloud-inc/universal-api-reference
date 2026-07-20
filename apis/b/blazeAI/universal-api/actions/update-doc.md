# Blaze AI: Update Doc

Updates an existing document in Blaze AI.

```
PUT https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/update-doc
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blaze AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/update-doc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspace_id": "994619",
  "id": "4981633",
  "docTitle": "AI Workflow Automation for Medium-to-Large Businesses: What to Automate First 🚀"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/update-doc', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspace_id": "994619",
    "id": "4981633",
    "docTitle": "AI Workflow Automation for Medium-to-Large Businesses: What to Automate First 🚀"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspace_id` | number | yes | Blaze workspace ID. Default: `994619`. |
| `id` | number | yes | Blaze document ID. Default: `4981633`. |
| `docTitle` | string | yes | Updated Blaze document title. Default: `AI Workflow Automation for Medium-to-Large Businesses: What to Automate First 🚀`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "createdAt": "string",
        "folderId": 1,
        "id": 1,
        "key": "string",
        "ownerId": 1,
        "title": "string",
        "updatedAt": "string",
        "workspaceId": 1
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
| `data.createdAt` | string |  |
| `data.folderId` | number |  |
| `data.id` | number |  |
| `data.key` | string |  |
| `data.ownerId` | number |  |
| `data.title` | string |  |
| `data.updatedAt` | string |  |
| `data.workspaceId` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Blaze AI API, this operation is `PATCH /api/v1/w/:workspace_id/docs/:id` (base URL `https://api.blaze.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-doc.md) for the provider-specific parameters and requirements.

