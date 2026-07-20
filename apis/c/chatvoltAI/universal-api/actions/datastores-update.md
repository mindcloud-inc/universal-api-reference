# Chatvolt AI: Update Datastore

Updates a datastore in Chatvolt AI.

```
PUT https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/datastores-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/datastores-update" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/datastores-update', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | ID of the datastore to be updated. |
| `name` | string | no | Name for application/json requests. |
| `description` | string | no | Description for application/json requests. |
| `type` | string | no | Type for application/json requests. |
| `isPublic` | boolean | no | IsPublic for application/json requests. |
| `pluginName` | string | no | PluginName for application/json requests. |
| `pluginDescriptionForHumans` | string | no | PluginDescriptionForHumans for application/json requests. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "isPublic": true,
      "name": "Ava Chen",
      "pluginDescriptionForHumans": "string",
      "pluginName": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Description. |
| `id` | string | Id. |
| `isPublic` | boolean | IsPublic. |
| `name` | string | Name. |
| `pluginDescriptionForHumans` | string | PluginDescriptionForHumans. |
| `pluginName` | string | PluginName. |
| `type` | string | Type. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `PATCH /datastores/{id}` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/datastores-update.md) for the provider-specific parameters and requirements.

