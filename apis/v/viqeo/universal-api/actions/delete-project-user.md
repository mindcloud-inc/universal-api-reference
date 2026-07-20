# Viqeo: Delete Project User

Deletes an existing project user from Viqeo.

```
DELETE https://connect.mindcloud.co/v1/universal/viqeo/latest/actions/delete-project-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viqeo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/viqeo/latest/actions/delete-project-user?connectionId=$CONNECTION_ID&projectId=string&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viqeo/latest/actions/delete-project-user?${params}`, {
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
| `projectId` | string | yes | Project identifier from the path. |
| `email` | string | yes | Project user email address. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viqeo API returns.

## Native endpoint

Through the native Viqeo API, this operation is `DELETE /media-platform/v1/project/:projectId/user/:email` (base URL `https://api.viqeo.tv`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-project-user.md) for the provider-specific parameters and requirements.

