# Mode: Delete Group Membership

Remove a member from a group in a Mode workspace.

```
DELETE https://connect.mindcloud.co/v1/universal/mode/latest/actions/delete-group-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mode/latest/actions/delete-group-membership?connectionId=$CONNECTION_ID&groupToken=string&membershipToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupToken": "string",
  "membershipToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mode/latest/actions/delete-group-membership?${params}`, {
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
| `groupToken` | string | yes | Mode group token. |
| `membershipToken` | string | yes | Mode group membership token. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Links": {},
      "memberToken": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Links` | object | Mode HAL links. |
| `memberToken` | string | Mode member token. |
| `token` | string | Mode group membership token. |

## Native endpoint

Through the native Mode API, this operation is `DELETE /groups/[:groupToken]/memberships/[:membershipToken]` (base URL `https://app.mode.com/api/{{credentials.workspace}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-group-membership.md) for the provider-specific parameters and requirements.

