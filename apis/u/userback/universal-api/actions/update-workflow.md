# Userback: Update Workflow

Updates a workflow in Userback.

```
PUT https://connect.mindcloud.co/v1/universal/userback/latest/actions/update-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userback `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/userback/latest/actions/update-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "563469",
  "name": "Temp Workflow 1419 Updated",
  "color": "#FF8800"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userback/latest/actions/update-workflow', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "563469",
    "name": "Temp Workflow 1419 Updated",
    "color": "#FF8800"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The workflow ID to update. Example: `563469`. |
| `name` | string | yes | The updated workflow name. Example: `Temp Workflow 1419 Updated`. |
| `color` | string | yes | The updated workflow color in hex format. Example: `#FF8800`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "id": 1,
      "name": "Ava Chen",
      "project": {
        "created": "string",
        "createdBy": 1,
        "id": 1,
        "isArchived": true,
        "name": "Ava Chen"
      },
      "sort": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `id` | number |  |
| `name` | string |  |
| `project.created` | string |  |
| `project.createdBy` | number |  |
| `project.id` | number |  |
| `project.isArchived` | boolean |  |
| `project.name` | string |  |
| `sort` | number |  |

## Native endpoint

Through the native Userback API, this operation is `PATCH /workflow/:id` (base URL `https://rest.userback.io/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workflow.md) for the provider-specific parameters and requirements.

