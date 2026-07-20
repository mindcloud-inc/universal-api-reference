# Tally: Cancel Invite



```
DELETE https://connect.mindcloud.co/v1/universal/tally/latest/actions/cancel-invite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tally `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/tally/latest/actions/cancel-invite?connectionId=$CONNECTION_ID&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tally/latest/actions/cancel-invite?${params}`, {
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
| `organizationId` | list<string> | yes |  |
| `inviteId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Tally API returns.

## Native endpoint

Through the native Tally API, this operation is `GET organizations/:organizationId/invites/:inviteId` (base URL `https://api.tally.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-invite.md) for the provider-specific parameters and requirements.

