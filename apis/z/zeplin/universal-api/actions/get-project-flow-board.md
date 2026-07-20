# Zeplin: Get Project Flow Board

Retrieves a project flow board from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/get-project-flow-board
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/get-project-flow-board?connectionId=$CONNECTION_ID&projectId=string&flowBoardId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "flowBoardId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/get-project-flow-board?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "number_of_connectors": 1,
      "number_of_groups": 1,
      "number_of_nodes": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `number_of_connectors` | number |  |
| `number_of_groups` | number |  |
| `number_of_nodes` | number |  |

## Native endpoint

Through the native Zeplin API, this operation is `GET /projects/{project_id}/flow_boards/{flow_board_id}` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-flow-board.md) for the provider-specific parameters and requirements.

