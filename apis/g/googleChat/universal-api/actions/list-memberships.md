# Google Chat: List Memberships

Retrieves memberships in a Google Chat space.

```
GET https://connect.mindcloud.co/v1/universal/googleChat/latest/actions/list-memberships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Chat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleChat/latest/actions/list-memberships?connectionId=$CONNECTION_ID&limit=25&offset=0&space=4Oe1TyAAAAE" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "space": "4Oe1TyAAAAE"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleChat/latest/actions/list-memberships?${params}`, {
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
| `space` | string | yes | Enter only the space ID from the List Spaces result. If the result shows spaces/4Oe1TyAAAAE, enter 4Oe1TyAAAAE here. Example: `4Oe1TyAAAAE`. |
| `filter` | string | no | Optional. Filter memberships by supported member fields. |
| `showGroups` | boolean | no | Optional. Include group memberships when true. |
| `showInvited` | boolean | no | Optional. Include invited memberships when true. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Chat API returns.

## Native endpoint

Through the native Google Chat API, this operation is `GET /spaces/:space/members` (base URL `https://chat.googleapis.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-memberships.md) for the provider-specific parameters and requirements.

