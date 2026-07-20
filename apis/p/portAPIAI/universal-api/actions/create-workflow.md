# Port API AI: Create Workflow

Creates a workflow in Port.

```
POST https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/create-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/create-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "string",
  "nodes[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/create-workflow', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "string",
    "nodes[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identifier` | string | yes |  |
| `title` | string | no |  |
| `icon` | string | no |  |
| `nodes[]` | array<object> | yes |  |
| `connections[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true,
      "workflow": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean |  |
| `workflow` | object |  |

## Native endpoint

Through the native Port API AI API, this operation is `POST /workflows` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workflow.md) for the provider-specific parameters and requirements.

