# Zeplin: Get Project Flow Board Node

Retrieves a project flow board node from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/get-project-flow-board-node
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/get-project-flow-board-node?connectionId=$CONNECTION_ID&projectId=string&flowBoardId=string&nodeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "flowBoardId": "string",
  "nodeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/get-project-flow-board-node?${params}`, {
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
| `projectId` | string | yes | Project id |
| `flowBoardId` | string | yes | Flow Board id |
| `nodeId` | string | yes | Board node id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "position": {},
      "screen": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `position` | object |  |
| `screen` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Zeplin API, this operation is `GET /projects/{project_id}/flow_boards/{flow_board_id}/nodes/{node_id}` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-flow-board-node.md) for the provider-specific parameters and requirements.

