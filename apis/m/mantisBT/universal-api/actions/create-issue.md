# MantisBT: Create Issue

Creates a new issue in MantisBT.

```
POST https://connect.mindcloud.co/v1/universal/mantisBT/latest/actions/create-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MantisBT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mantisBT/latest/actions/create-issue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "category.name": "Ava Chen",
  "description": "string",
  "project.id": 1,
  "summary": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mantisBT/latest/actions/create-issue', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "category.name": "Ava Chen",
    "description": "string",
    "project.id": 1,
    "summary": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `category.name` | string | yes | Existing category name for the issue, such as General |
| `description` | string | yes | Issue description |
| `project.id` | number | yes | Project ID where the issue will be created |
| `summary` | string | yes | Issue summary |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MantisBT API returns.

## Native endpoint

Through the native MantisBT API, this operation is `POST /issues` (base URL `{{credentials.baseUrl}}/api/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-issue.md) for the provider-specific parameters and requirements.

