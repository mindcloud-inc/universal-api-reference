# DevCycle: List Variables

Retrieves variables from DevCycle.

```
GET https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/list-variables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DevCycle `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/list-variables?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/list-variables?${params}`, {
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
| `project` | string | no | Project key. Default: `mindcloud`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "createdBy": "string",
      "description": "string",
      "featureId": "string",
      "id": "string",
      "key": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "source": "string",
      "status": "string",
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
| `createdAt` | string |  |
| `createdBy` | string |  |
| `description` | string |  |
| `featureId` | string |  |
| `id` | string |  |
| `key` | string |  |
| `name` | string |  |
| `projectId` | string |  |
| `source` | string |  |
| `status` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native DevCycle API, this operation is `GET /v1/projects/:project/variables` (base URL `https://api.devcycle.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-variables.md) for the provider-specific parameters and requirements.

