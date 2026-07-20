# Blaze AI: Add Doc Property

Creates a document property in Blaze AI.

```
POST https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/add-doc-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blaze AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/add-doc-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspace_id": "994619",
  "doc_id": "4981633",
  "propertyId": "22343659"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/add-doc-property', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspace_id": "994619",
    "doc_id": "4981633",
    "propertyId": "22343659"
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
| `propertyId` | number | yes | Workspace property ID. Default: `22343659`. |
| `value` | string | no | Property value. Default: `Codex Choice`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "id": 1,
        "property": {
          "defaultForArticles": true,
          "id": 1,
          "name": "Ava Chen",
          "type": "string"
        },
        "value": "string"
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
| `data.id` | number |  |
| `data.property.defaultForArticles` | boolean |  |
| `data.property.id` | number |  |
| `data.property.name` | string |  |
| `data.property.type` | string |  |
| `data.value` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Blaze AI API, this operation is `POST /api/v1/w/:workspace_id/docs/:doc_id/properties` (base URL `https://api.blaze.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-doc-property.md) for the provider-specific parameters and requirements.

