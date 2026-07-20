# Anthropic: Delete Invite

Deletes an invite from the Anthropic organization.

```
DELETE https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/delete-invite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anthropic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/delete-invite?connectionId=$CONNECTION_ID&inviteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inviteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/delete-invite?${params}`, {
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
| `inviteId` | string | yes | Unique ID of the invite to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Deleted invite ID. |
| `type` | string | Object type. |

## Native endpoint

Through the native Anthropic API, this operation is `DELETE /v1/organizations/invites/{invite_id}` (base URL `https://api.anthropic.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-invite.md) for the provider-specific parameters and requirements.

