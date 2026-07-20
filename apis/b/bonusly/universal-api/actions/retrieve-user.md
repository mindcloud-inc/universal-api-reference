# Bonusly: Retrieve User

Retrieves a user from Bonusly.

```
GET https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/retrieve-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bonusly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/retrieve-user?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/retrieve-user?${params}`, {
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
| `id` | string | yes | The Bonusly user ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "displayName": "Ava Chen",
      "earningBalance": 1,
      "email": "ava@example.com",
      "givingBalance": 1,
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `displayName` | string |  |
| `earningBalance` | number |  |
| `email` | string |  |
| `givingBalance` | number |  |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Bonusly API, this operation is `GET /users/:id` (base URL `https://bonus.ly/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-user.md) for the provider-specific parameters and requirements.

