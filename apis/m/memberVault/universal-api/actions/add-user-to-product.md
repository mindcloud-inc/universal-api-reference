# MemberVault: Add User to Product

Adds a user to a MemberVault product, creating them if needed.

```
POST https://connect.mindcloud.co/v1/universal/memberVault/latest/actions/add-user-to-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MemberVault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/memberVault/latest/actions/add-user-to-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "courseKey": "string",
  "email": "ava@example.com",
  "firstName": "Ava",
  "lastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/memberVault/latest/actions/add-user-to-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "courseKey": "string",
    "email": "ava@example.com",
    "firstName": "Ava",
    "lastName": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `courseKey` | string | yes | The MemberVault course key for the target course. |
| `email` | string | yes | The email address for the user to add. |
| `firstName` | string | yes | The user's first name. |
| `lastName` | string | yes | The user's last name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `userId` | string |  |

## Native endpoint

Through the native MemberVault API, this operation is `GET /add_user` (base URL `https://{{credentials.accountName}}.mvsite.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-user-to-product.md) for the provider-specific parameters and requirements.

