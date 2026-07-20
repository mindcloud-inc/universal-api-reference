# Atriomail: Delete User



```
DELETE https://connect.mindcloud.co/v1/universal/atriomail/latest/actions/delete-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atriomail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/atriomail/latest/actions/delete-user?connectionId=$CONNECTION_ID&userId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atriomail/latest/actions/delete-user?${params}`, {
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
| `userId` | number | yes | The AtrioMail user ID. |

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
| `message` | string |  |

## Native endpoint

Through the native Atriomail API, this operation is `DELETE /users/:userId` (base URL `https://system.atriomail.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-user.md) for the provider-specific parameters and requirements.

