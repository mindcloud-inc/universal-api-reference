# Faithlife: Delete Membership

Deletes a group membership from Faithlife.

```
DELETE https://connect.mindcloud.co/v1/universal/faithlife/latest/actions/delete-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Faithlife `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/faithlife/latest/actions/delete-membership?connectionId=$CONNECTION_ID&membershipId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "membershipId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/faithlife/latest/actions/delete-membership?${params}`, {
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
| `membershipId` | string | yes | The Faithlife membership ID to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Faithlife API returns.

## Native endpoint

Through the native Faithlife API, this operation is `DELETE /memberships/:membershipId` (base URL `https://accountsapi.logos.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-membership.md) for the provider-specific parameters and requirements.

