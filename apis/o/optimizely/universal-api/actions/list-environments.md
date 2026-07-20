# Optimizely: List Environments

Retrieves a list of environments from Optimizely.

```
GET https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/list-environments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optimizely `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/list-environments?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=4844790198566912" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "4844790198566912"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/list-environments?${params}`, {
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
| `projectId` | string | yes | Filter environments to one project. Default: `4844790198566912`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "created": "string",
      "description": "string",
      "hasRestrictedPermissions": true,
      "id": 1,
      "isPrimary": true,
      "key": "string",
      "lastModified": "string",
      "name": "Ava Chen",
      "priority": 1,
      "projectId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `created` | string |  |
| `description` | string |  |
| `hasRestrictedPermissions` | boolean |  |
| `id` | number |  |
| `isPrimary` | boolean |  |
| `key` | string |  |
| `lastModified` | string |  |
| `name` | string |  |
| `priority` | number |  |
| `projectId` | number |  |

## Native endpoint

Through the native Optimizely API, this operation is `GET /environments` (base URL `https://api.optimizely.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-environments.md) for the provider-specific parameters and requirements.

