# Aloware: List Users

Retrieves user records from your Aloware account.

```
GET https://connect.mindcloud.co/v1/universal/aloware/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aloware `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aloware/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aloware/latest/actions/list-users?${params}`, {
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
| `email` | string | no | Optional user email to look up a specific user record. |
| `userId` | string | no | Optional Aloware user ID to look up a specific user record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentStatus": 1,
      "email": "ava@example.com",
      "humanReadableAgentStatus": "string",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentStatus` | number |  |
| `email` | string |  |
| `humanReadableAgentStatus` | string |  |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Aloware API, this operation is `GET /api/v1/webhook/users` (base URL `https://app.aloware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

