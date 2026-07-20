# Testomato: Project users

Retrieves project users from Testomato.

```
GET https://connect.mindcloud.co/v1/universal/testomato/latest/actions/project-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testomato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testomato/latest/actions/project-users?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testomato/latest/actions/project-users?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canBeRemoved": true,
      "confirmed": true,
      "email": "ava@example.com",
      "id": 1,
      "isPayer": true,
      "notificationDelay": 1,
      "reportPeriod": "string",
      "role": {},
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canBeRemoved` | boolean |  |
| `confirmed` | boolean |  |
| `email` | string |  |
| `id` | number |  |
| `isPayer` | boolean |  |
| `notificationDelay` | number |  |
| `reportPeriod` | string |  |
| `role` | object |  |
| `timezone` | string |  |

## Native endpoint

Through the native Testomato API, this operation is `GET /project/:id/users` (base URL `https://testomato.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/project-users.md) for the provider-specific parameters and requirements.

