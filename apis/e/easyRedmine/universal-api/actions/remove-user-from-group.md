# Easy Redmine: Remove User From Group

Removes a user from a group in Easy Redmine.

```
DELETE https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/remove-user-from-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy Redmine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/remove-user-from-group?connectionId=$CONNECTION_ID&id=1&userId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "userId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/remove-user-from-group?${params}`, {
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
| `id` | number | yes | ID of the group to remove a user from. |
| `userId` | number | yes | ID of the user to remove from the group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "success": true,
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `success` | boolean |  |
| `userId` | number |  |

## Native endpoint

Through the native Easy Redmine API, this operation is `DELETE /groups/:id/users/:userId.json` (base URL `https://3f73561b8b.bigus-e5.easy8.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-user-from-group.md) for the provider-specific parameters and requirements.

