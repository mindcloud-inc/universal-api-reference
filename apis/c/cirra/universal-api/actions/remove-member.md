# Cirra: Remove Member

Deletes a Cirra member by user ID.

```
DELETE https://connect.mindcloud.co/v1/universal/cirra/latest/actions/remove-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cirra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cirra/latest/actions/remove-member?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cirra/latest/actions/remove-member?${params}`, {
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
| `userId` | list | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": "string",
      "isAdmin": true,
      "roleId": "string",
      "user": {
        "email": "ava@example.com",
        "isPending": true,
        "name": "Ava Chen"
      },
      "userId": "string",
      "workflowCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | string |  |
| `isAdmin` | boolean |  |
| `roleId` | string |  |
| `user.email` | string |  |
| `user.isPending` | boolean |  |
| `user.name` | string |  |
| `userId` | string |  |
| `workflowCount` | number |  |

## Native endpoint

Through the native Cirra API, this operation is `DELETE /v1/members/:userId` (base URL `http://api-public:9801`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-member.md) for the provider-specific parameters and requirements.

