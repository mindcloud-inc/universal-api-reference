# Google Groups: Delete Group Alias

Deletes a group alias from Google Groups.

```
DELETE https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/delete-group-alias
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Groups `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/delete-group-alias?connectionId=$CONNECTION_ID&groupKey=string&alias=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupKey": "string",
  "alias": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleGroups/latest/actions/delete-group-alias?${params}`, {
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
| `groupKey` | string | yes | The group email address, group alias, or unique group ID. |
| `alias` | string | yes | The alias email address to delete from the group. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Groups API returns.

## Native endpoint

Through the native Google Groups API, this operation is `DELETE https://admin.googleapis.com/admin/directory/v1/groups/:groupKey/aliases/:alias` (base URL `https://groups.google.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-group-alias.md) for the provider-specific parameters and requirements.

