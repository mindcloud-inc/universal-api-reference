# Optimizely: Search Entities

Finds entities in Optimizely by search query.

```
GET https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/search-entities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optimizely `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/search-entities?connectionId=$CONNECTION_ID&limit=25&offset=0&query=test" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "query": "test"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/search-entities?${params}`, {
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
| `query` | string | yes | The search text. Default: `test`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "description": "string",
      "enabled": true,
      "experimentCount": 1,
      "id": 1,
      "key": "string",
      "lastModified": "string",
      "name": "Ava Chen",
      "platform": "string",
      "projectId": 1,
      "projectName": "Ava Chen",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `description` | string |  |
| `enabled` | boolean |  |
| `experimentCount` | number |  |
| `id` | number |  |
| `key` | string |  |
| `lastModified` | string |  |
| `name` | string |  |
| `platform` | string |  |
| `projectId` | number |  |
| `projectName` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Optimizely API, this operation is `GET /search` (base URL `https://api.optimizely.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-entities.md) for the provider-specific parameters and requirements.

