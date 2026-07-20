# Socie: Delete Group Membership



```
DELETE https://connect.mindcloud.co/v1/universal/socie/latest/actions/delete-group-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/socie/latest/actions/delete-group-membership?connectionId=$CONNECTION_ID&groupIdentifier=string&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupIdentifier": "string",
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socie/latest/actions/delete-group-membership?${params}`, {
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
| `groupIdentifier` | string | yes | The Socie id or externalId of the group. |
| `identifier` | string | yes | The Socie id or externalId of the group membership. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Socie API returns.

## Native endpoint

Through the native Socie API, this operation is `DELETE /api/v1/groups/:groupIdentifier/memberships/:identifier` (base URL `https://api.socie.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-group-membership.md) for the provider-specific parameters and requirements.

