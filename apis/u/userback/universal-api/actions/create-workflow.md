# Userback: Create Workflow

Creates a new workflow in Userback.

```
POST https://connect.mindcloud.co/v1/universal/userback/latest/actions/create-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userback `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/userback/latest/actions/create-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "137605",
  "name": "QA Triage",
  "color": "#6AB295"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userback/latest/actions/create-workflow', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "137605",
    "name": "QA Triage",
    "color": "#6AB295"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | The project ID that will own the workflow. Example: `137605`. |
| `name` | string | yes | The workflow name. Example: `QA Triage`. |
| `color` | string | yes | The workflow color in hex format. Example: `#6AB295`. |

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

Through the native Userback API, this operation is `POST /workflow` (base URL `https://rest.userback.io/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workflow.md) for the provider-specific parameters and requirements.

