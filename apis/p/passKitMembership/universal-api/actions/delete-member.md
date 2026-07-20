# PassKit Membership: Delete Member

Deletes an existing member from PassKit Membership.

```
DELETE https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/delete-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Membership `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/delete-member?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/delete-member?${params}`, {
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
| `id` | string | yes | PassKit member id to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PassKit Membership API returns.

## Native endpoint

Through the native PassKit Membership API, this operation is `DELETE /members/member` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-member.md) for the provider-specific parameters and requirements.

