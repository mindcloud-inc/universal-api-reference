# Alpha TransForm: Delete User Roles In Account

Deletes a user's account roles from Alpha TransForm.

```
DELETE https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/delete-user-roles-in-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alpha TransForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/delete-user-roles-in-account?connectionId=$CONNECTION_ID&userIdToDelete=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userIdToDelete": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/delete-user-roles-in-account?${params}`, {
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
| `userId` | string | no | UserId |
| `userIdToDelete` | string | yes |  |
| `roles` | string | no | Comma delimited list of roles |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Alpha TransForm API returns.

## Native endpoint

Through the native Alpha TransForm API, this operation is `GET /deleteUserRolesInAccount/:userIdToDelete` (base URL `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-user-roles-in-account.md) for the provider-specific parameters and requirements.

