# Blaze AI: Create Workspace Property

Creates a workspace property in Blaze AI.

```
POST https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/create-workspace-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blaze AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/create-workspace-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspace_id": "994619",
  "propertyName": "Codex Temp Property",
  "propertyType": "single_select",
  "propertyValue": "Codex Choice"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/create-workspace-property', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspace_id": "994619",
    "propertyName": "Codex Temp Property",
    "propertyType": "single_select",
    "propertyValue": "Codex Choice"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspace_id` | number | yes | Default: `994619`. |
| `propertyName` | string | yes | Default: `Codex Temp Property`. |
| `propertyType` | string | yes | Default: `single_select`. |
| `defaultForArticles` | boolean | no |  |
| `dateFormat` | string | no |  |
| `numberFormat` | string | no |  |
| `allowMentioningMultiplePeople` | boolean | no |  |
| `notifyPerson` | boolean | no |  |
| `propertyValue` | string | yes | Default: `Codex Choice`. |
| `propertyValueColor` | string | no | Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "defaultForArticles": true,
        "id": 1,
        "meta": {
          "dateFormat": "string",
          "numberFormat": "string"
        },
        "name": "Ava Chen",
        "type": "string"
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
| `data.defaultForArticles` | boolean |  |
| `data.id` | number |  |
| `data.meta.dateFormat` | string |  |
| `data.meta.numberFormat` | string |  |
| `data.name` | string |  |
| `data.type` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Blaze AI API, this operation is `POST /api/v1/w/:workspace_id/properties` (base URL `https://api.blaze.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workspace-property.md) for the provider-specific parameters and requirements.

