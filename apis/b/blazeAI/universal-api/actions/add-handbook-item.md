# Blaze AI: Add Handbook Item

Creates a handbook item in Blaze AI.

```
POST https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/add-handbook-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blaze AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/add-handbook-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspace_id": "994619",
  "handbook_id": "3412870",
  "itemType": "doc",
  "docId": "4981633",
  "title": "AI Workflow Automation for Medium-to-Large Businesses: What to Automate First 🚀",
  "url": "https://app.blaze.ai/workspaces/994619/files"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/add-handbook-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspace_id": "994619",
    "handbook_id": "3412870",
    "itemType": "doc",
    "docId": "4981633",
    "title": "AI Workflow Automation for Medium-to-Large Businesses: What to Automate First 🚀",
    "url": "https://app.blaze.ai/workspaces/994619/files"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspace_id` | number | yes | Default: `994619`. |
| `handbook_id` | number | yes | Default: `3412870`. |
| `itemType` | string | yes | Default: `doc`. |
| `position` | number | no |  |
| `parentItemId` | string | no |  |
| `docId` | number | yes | Default: `4981633`. |
| `title` | string | yes | Default: `AI Workflow Automation for Medium-to-Large Businesses: What to Automate First 🚀`. |
| `url` | string | yes | Default: `https://app.blaze.ai/workspaces/994619/files`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "docId": 1,
        "handbookId": 1,
        "id": 1,
        "parentItemId": 1,
        "position": 1,
        "title": "string",
        "type": "string",
        "url": "https://example.com"
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
| `data.docId` | number |  |
| `data.handbookId` | number |  |
| `data.id` | number |  |
| `data.parentItemId` | number |  |
| `data.position` | number |  |
| `data.title` | string |  |
| `data.type` | string |  |
| `data.url` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Blaze AI API, this operation is `POST /api/v1/w/:workspace_id/handbooks/:handbook_id/items` (base URL `https://api.blaze.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-handbook-item.md) for the provider-specific parameters and requirements.

