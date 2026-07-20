# Google Workspace Admin: Delete Group

Deletes an existing group from Google Workspace Admin.

```
DELETE https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/delete-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Workspace Admin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/delete-group?connectionId=$CONNECTION_ID&groupKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/delete-group?${params}`, {
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

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Workspace Admin API returns.

## Native endpoint

Through the native Google Workspace Admin API, this operation is `DELETE /admin/directory/v1/groups/:groupKey` (base URL `https://admin.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-group.md) for the provider-specific parameters and requirements.

