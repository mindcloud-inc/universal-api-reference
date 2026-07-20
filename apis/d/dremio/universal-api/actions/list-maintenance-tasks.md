# Dremio: List Maintenance Tasks

Retrieves maintenance tasks from a Dremio project.

```
GET https://connect.mindcloud.co/v1/universal/dremio/latest/actions/list-maintenance-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dremio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dremio/latest/actions/list-maintenance-tasks?connectionId=$CONNECTION_ID&filter=type%3D%3D%22OPTIMIZE%22%26%26level%3D%3D%22TABLE%22&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filter": "type==\"OPTIMIZE\"&&level==\"TABLE\"",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dremio/latest/actions/list-maintenance-tasks?${params}`, {
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
| `filter` | string | yes | Common Expression Language (CEL) filter, for example type=="OPTIMIZE"&&level=="TABLE". Default: `type==\"OPTIMIZE\"&&level==\"TABLE\"`. |
| `projectId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "nextPageToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `nextPageToken` | string |  |

## Native endpoint

Through the native Dremio API, this operation is `GET /projects/:project_id/maintenance/tasks` (base URL `https://api.dremio.cloud/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-maintenance-tasks.md) for the provider-specific parameters and requirements.

