# Jitbit Helpdesk: List Subscribers



```
GET https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jitbit Helpdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-subscribers?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-subscribers?${params}`, {
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
| `id` | number | yes | Jitbit ticket ID to list subscribers for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "disabled": true,
      "email": "ava@example.com",
      "fullName": "Ava Chen",
      "userId": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `disabled` | boolean | Whether the subscriber is disabled. |
| `email` | string | Subscriber email. |
| `fullName` | string | Subscriber full name. |
| `userId` | number | Subscriber user ID. |
| `username` | string | Subscriber username. |

## Native endpoint

Through the native Jitbit Helpdesk API, this operation is `GET /Subscribers` (base URL `{{credentials.helpdeskBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscribers.md) for the provider-specific parameters and requirements.

