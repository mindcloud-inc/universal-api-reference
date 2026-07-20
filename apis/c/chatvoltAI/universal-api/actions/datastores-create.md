# Chatvolt AI: Create Datastore

Creates a datastore in Chatvolt AI.

```
POST https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/datastores-create
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/datastores-create" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/datastores-create', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Datastore name. If not provided, a fun name will be generated automatically. |
| `description` | string | no | Datastore description. |
| `type` | string | yes | Datastore type (e.g., 'qdrant'). |
| `isPublic` | boolean | no | Defines whether the datastore is public (accessible without specific datastore authentication) or private. |
| `pluginName` | string | no | Short name for the OpenAI plugin associated with this datastore (optional, used if the datastore is exposed as a plugin). Maximum of 20 characters. |
| `pluginDescriptionForHumans` | string | no | Human-readable description for the OpenAI plugin (optional). Maximum of 90 characters. |

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

Through the native Chatvolt AI API, this operation is `POST /datastores` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/datastores-create.md) for the provider-specific parameters and requirements.

