# Nozbe Personal: Delete Project

Deletes an existing project from Nozbe Personal.

```
DELETE https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/delete-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nozbe Personal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/delete-project?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/delete-project?${params}`, {
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
| `id` | string | yes | Project ID to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nozbe Personal API returns.

## Native endpoint

Through the native Nozbe Personal API, this operation is `DELETE /projects/:id` (base URL `https://api4.nozbe.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-project.md) for the provider-specific parameters and requirements.

