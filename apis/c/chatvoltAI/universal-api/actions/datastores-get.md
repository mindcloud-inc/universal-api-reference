# Chatvolt AI: Get Datastore

Retrieves a datastore from Chatvolt AI.

```
GET https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/datastores-get
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/datastores-get?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/datastores-get?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | ID of the datastore to be retrieved. |
| `search` | string | no | Term to search for datasources by name (case-insensitive). Optional. |
| `status` | string | no | Filters datasources by status. Optional. |
| `type` | string | no | Filters datasources by type. Optional. |
| `offset` | number | no | Number of pages to skip for datasource pagination. Optional. |
| `limit` | number | no | Maximum number of datasources to return per page. Optional. |
| `groupId` | string | no | Filtra datasources por um ID de grupo específico. Opcional. |

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

Through the native Chatvolt AI API, this operation is `GET /datastores/{id}` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/datastores-get.md) for the provider-specific parameters and requirements.

