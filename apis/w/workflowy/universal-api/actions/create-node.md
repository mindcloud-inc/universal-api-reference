# Workflowy: Create Node

Creates a new node in Workflowy.

```
POST https://connect.mindcloud.co/v1/universal/workflowy/latest/actions/create-node
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workflowy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workflowy/latest/actions/create-node" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workflowy/latest/actions/create-node', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The text content of the new node. |
| `parentId` | string | no | Node UUID, target key like home or inbox, or None for a top-level node. |
| `note` | string | no | Additional note content for the node. |
| `layoutMode` | string | no | Display mode like bullets, todo, h1, h2, or h3. |
| `position` | string | no | Where to place the node: top or bottom. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "itemId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `itemId` | string | The identifier of the newly created node. |

## Native endpoint

Through the native Workflowy API, this operation is `POST /nodes` (base URL `https://workflowy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-node.md) for the provider-specific parameters and requirements.

