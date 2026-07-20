# Reward Sciences: Get User



```
GET https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reward Sciences `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rewardSciences/latest/actions/get-user?${params}`, {
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
| `userId` | number | yes | The Reward Sciences user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": 1,
      "custom_fields": {},
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "last_name": "Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number | Current rewards balance. |
| `custom_fields` | object | Custom user metadata. |
| `email` | string | Reward Sciences email address. |
| `first_name` | string | User first name. |
| `id` | number | User ID. |
| `last_name` | string | User last name. |

## Native endpoint

Through the native Reward Sciences API, this operation is `GET /users/:userId` (base URL `https://api.rewardsciences.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

