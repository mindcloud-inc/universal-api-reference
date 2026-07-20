# DevCycle: List Environments

Retrieves environments from DevCycle.

```
GET https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/list-environments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DevCycle `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/list-environments?connectionId=$CONNECTION_ID&limit=25&offset=0&project=mindcloud" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "project": "mindcloud"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/list-environments?${params}`, {
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
| `project` | string | yes | Project key or ID. Default: `mindcloud`. |
| `page` | number | no | Page number starting at 1. Default: `1`. |
| `perPage` | number | no | Maximum items to return, up to 1000. Default: `100`. |
| `sortBy` | string | no | Field to sort by. One of: `0`, `1`, `2`, `3`, `4`. |
| `sortOrder` | string | no | Sort direction. One of: `0`, `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `search` | string | no | Search term with minimum length 3. |
| `createdBy` | string | no | Filter by creator user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "createdAt": "string",
      "createdBy": "string",
      "id": "string",
      "key": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "readonly": true,
      "sdkKeys": {
        "client": [
          [
            {}
          ]
        ],
        "mobile": [
          [
            {}
          ]
        ],
        "server": [
          [
            {}
          ]
        ]
      },
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `createdAt` | string |  |
| `createdBy` | string |  |
| `id` | string |  |
| `key` | string |  |
| `name` | string |  |
| `projectId` | string |  |
| `readonly` | boolean |  |
| `sdkKeys.client[]` | array<object> |  |
| `sdkKeys.mobile[]` | array<object> |  |
| `sdkKeys.server[]` | array<object> |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native DevCycle API, this operation is `GET /v1/projects/:project/environments` (base URL `https://api.devcycle.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-environments.md) for the provider-specific parameters and requirements.

