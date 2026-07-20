# Alpha TransForm: Remove User From Account

Removes a user from an Alpha TransForm account.

```
DELETE https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/remove-user-from-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alpha TransForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/remove-user-from-account?connectionId=$CONNECTION_ID&accountToRemoveFrom=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountToRemoveFrom": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/remove-user-from-account?${params}`, {
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
| `userIdToRemove` | string | no | UserId to remove from TransForm account |
| `accountToRemoveFrom` | string | yes | Only super users can specify an accountId. Otherwise TransForm account associated with API key is used. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Alpha TransForm API returns.

## Native endpoint

Through the native Alpha TransForm API, this operation is `POST /removeUserFromTransFormAccount/:accountToRemoveFrom` (base URL `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-user-from-account.md) for the provider-specific parameters and requirements.

