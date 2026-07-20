# MantisBT: Get Project Users

Retrieves project users from a MantisBT project.

```
GET https://connect.mindcloud.co/v1/universal/mantisBT/latest/actions/get-project-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MantisBT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mantisBT/latest/actions/get-project-users?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mantisBT/latest/actions/get-project-users?${params}`, {
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
| `projectId` | number | yes | ID of the project whose users to return |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MantisBT API returns.

## Native endpoint

Through the native MantisBT API, this operation is `GET /projects/{project_id}/users` (base URL `{{credentials.baseUrl}}/api/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-users.md) for the provider-specific parameters and requirements.

