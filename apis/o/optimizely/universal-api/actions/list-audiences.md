# Optimizely: List Audiences

Retrieves a list of audiences from Optimizely.

```
GET https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/list-audiences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optimizely `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/list-audiences?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=4844790198566912" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "4844790198566912"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/list-audiences?${params}`, {
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
| `projectId` | string | yes | Filter audiences to one project. Default: `4844790198566912`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "created": "string",
      "description": "string",
      "experimentCount": 1,
      "id": 1,
      "isClassic": true,
      "lastModified": "string",
      "name": "Ava Chen",
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
| `experimentCount` | number |  |
| `id` | number |  |
| `isClassic` | boolean |  |
| `lastModified` | string |  |
| `name` | string |  |
| `projectId` | number |  |

## Native endpoint

Through the native Optimizely API, this operation is `GET /audiences` (base URL `https://api.optimizely.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-audiences.md) for the provider-specific parameters and requirements.

