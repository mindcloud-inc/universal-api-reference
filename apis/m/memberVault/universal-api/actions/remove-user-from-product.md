# MemberVault: Remove User from Product

Removes a user's access to a product in MemberVault.

```
DELETE https://connect.mindcloud.co/v1/universal/memberVault/latest/actions/remove-user-from-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MemberVault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/memberVault/latest/actions/remove-user-from-product?connectionId=$CONNECTION_ID&courseKey=string&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "courseKey": "string",
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/memberVault/latest/actions/remove-user-from-product?${params}`, {
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
| `courseKey` | string | yes | The MemberVault course key for the target course. |
| `email` | string | yes | The email address for the user to remove. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider message describing the removal result. |

## Native endpoint

Through the native MemberVault API, this operation is `GET /remove_user` (base URL `https://{{credentials.accountName}}.mvsite.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-user-from-product.md) for the provider-specific parameters and requirements.

