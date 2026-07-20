# Cinode: Remove Project Assignment Tag

Removes a tag from a project assignment in Cinode.

```
DELETE https://connect.mindcloud.co/v1/universal/cinode/latest/actions/remove-project-assignment-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cinode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cinode/latest/actions/remove-project-assignment-tag?connectionId=$CONNECTION_ID&companyId=1&projectId=1&roleId=1&tagId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "1",
  "projectId": "1",
  "roleId": "1",
  "tagId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cinode/latest/actions/remove-project-assignment-tag?${params}`, {
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
| `companyId` | number | yes | Cinode company identifier. |
| `projectId` | number | yes | Identifier of the project. |
| `roleId` | number | yes | Identifier of the project assignment role. |
| `tagId` | number | yes | Identifier of the tag to remove. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cinode API returns.

## Native endpoint

Through the native Cinode API, this operation is `DELETE /v0.2/companies/:companyId/projects/:projectId/roles/:roleId/tags/:tagId` (base URL `https://api.cinode.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-project-assignment-tag.md) for the provider-specific parameters and requirements.

