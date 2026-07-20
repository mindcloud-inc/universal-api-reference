# Alpha TransForm: Add User To Account

Adds a user to an Alpha TransForm account.

```
POST https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/add-user-to-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alpha TransForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/add-user-to-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/add-user-to-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | no | UserId to add to TransForm account |
| `roles` | string | no | Roles for user in this TransForm account |
| `validateUser` | boolean | no | If true only people with valid TransForm user accounts are added |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Alpha TransForm API returns.

## Native endpoint

Through the native Alpha TransForm API, this operation is `GET /addUserToTransFormAccount/` (base URL `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-user-to-account.md) for the provider-specific parameters and requirements.

