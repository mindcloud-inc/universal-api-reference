# Zeplin: Update Project Component

Updates an existing project component in Zeplin.

```
PUT https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/update-project-component
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/update-project-component" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "componentId": "string",
  "description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/update-project-component', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "componentId": "string",
    "description": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Project id |
| `componentId` | string | yes | Component id |
| `description` | string | yes | New description for component |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zeplin API returns.

## Native endpoint

Through the native Zeplin API, this operation is `PATCH /projects/{project_id}/components/{component_id}` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project-component.md) for the provider-specific parameters and requirements.

