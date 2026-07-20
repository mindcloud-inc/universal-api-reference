# EARLY: Remove Member from Folder

Removes a member from an EARLY folder.

```
DELETE https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/remove-member-from-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EARLY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/remove-member-from-folder?connectionId=$CONNECTION_ID&folderId=340665&memberId=999999" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "340665",
  "memberId": "999999"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/remove-member-from-folder?${params}`, {
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
| `folderId` | string | yes | Folder ID. Default: `340665`. |
| `memberId` | string | yes | Folder member ID. Default: `999999`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EARLY API returns.

## Native endpoint

Through the native EARLY API, this operation is `DELETE /api/v4/folders/:folderId/members/:memberId` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-member-from-folder.md) for the provider-specific parameters and requirements.

