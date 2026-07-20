# DevCycle: List Webhooks

Retrieves webhooks from DevCycle.

```
GET https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DevCycle `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/list-webhooks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devCycle/latest/actions/list-webhooks?${params}`, {
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
      "environmentIds": [
        [
          "string"
        ]
      ],
      "events": [
        [
          "string"
        ]
      ],
      "featureId": "string",
      "id": "string",
      "name": "Ava Chen",
      "outputFormat": "string",
      "projectId": "string",
      "source": "string",
      "updatedAt": "string",
      "url": "https://example.com"
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
| `environmentIds[]` | array<string> |  |
| `events[]` | array<string> |  |
| `featureId` | string |  |
| `id` | string |  |
| `name` | string |  |
| `outputFormat` | string |  |
| `projectId` | string |  |
| `source` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |

## Native endpoint

Through the native DevCycle API, this operation is `GET /v1/projects/:project/webhooks` (base URL `https://api.devcycle.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

