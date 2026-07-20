# FTrack: Check Permissions

Checks permissions in FTrack for an entity.

```
GET https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/check-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FTrack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/check-permissions?connectionId=$CONNECTION_ID&entityType=Task&entityData=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entityType": "Task",
  "entityData": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/check-permissions?${params}`, {
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
| `entityType` | string | yes | Entity type whose permissions should be evaluated. Example: `Task`. |
| `entityData` | object | yes | Entity payload used for the permission check. |
| `expression` | string | no | Optional permission expression to evaluate. Example: `update`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native FTrack API returns.

## Native endpoint

Through the native FTrack API, this operation is `POST /api` (base URL `{{credentials.serverUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-permissions.md) for the provider-specific parameters and requirements.

