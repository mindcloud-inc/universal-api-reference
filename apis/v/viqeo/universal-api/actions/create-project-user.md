# Viqeo: Create Project User

Creates a new project user in Viqeo.

```
POST https://connect.mindcloud.co/v1/universal/viqeo/latest/actions/create-project-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viqeo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viqeo/latest/actions/create-project-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "email": "ava@example.com",
  "locale": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viqeo/latest/actions/create-project-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "email": "ava@example.com",
    "locale": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Project identifier from the path. |
| `email` | string | yes | User email address. |
| `locale` | string | yes | User locale, for example en. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viqeo API returns.

## Native endpoint

Through the native Viqeo API, this operation is `PUT /media-platform/v1/project/:projectId/user` (base URL `https://api.viqeo.tv`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-user.md) for the provider-specific parameters and requirements.

