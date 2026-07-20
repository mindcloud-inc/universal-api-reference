# Google Workspace Admin: Remove Group Member

Removes a member from a Google Workspace Admin group.

```
DELETE https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/remove-group-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Workspace Admin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/remove-group-member?connectionId=$CONNECTION_ID&groupKey=string&memberKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupKey": "string",
  "memberKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/remove-group-member?${params}`, {
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
| `groupKey` | string | yes | Group email address, alias, or unique ID. |
| `memberKey` | string | yes | Member email address, alias, or unique ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Workspace Admin API returns.

## Native endpoint

Through the native Google Workspace Admin API, this operation is `DELETE /admin/directory/v1/groups/:groupKey/members/:memberKey` (base URL `https://admin.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-group-member.md) for the provider-specific parameters and requirements.

