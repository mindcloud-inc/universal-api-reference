# Asana: Get memberships from a project

Retrieves project memberships from Asana.

```
GET https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-memberships-from-a-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-memberships-from-a-project?connectionId=$CONNECTION_ID&limit=25&offset=0&projectGid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectGid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-memberships-from-a-project?${params}`, {
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
| `projectGid` | string | yes | Asana project gid parameter. |
| `user` | string | no | Asana user parameter. |
| `opt_pretty` | boolean | no | Asana opt pretty parameter. |
| `limit` | number | no | Asana limit parameter. |
| `offset` | string | no | Asana offset parameter. |
| `opt_fields` | list<string> | no | Asana opt fields parameter. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Asana API returns.

## Native endpoint

Through the native Asana API, this operation is `GET projects/:project_gid/project_memberships` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-memberships-from-a-project.md) for the provider-specific parameters and requirements.

