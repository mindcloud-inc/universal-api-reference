# Testomato: Add user to project

Adds a user to a Testomato project.

```
POST https://connect.mindcloud.co/v1/universal/testomato/latest/actions/add-user-to-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testomato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/testomato/latest/actions/add-user-to-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "email": "ava@example.com",
  "role": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testomato/latest/actions/add-user-to-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "email": "ava@example.com",
    "role": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `email` | string | yes |  |
| `role` | number | yes |  |

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

Through the native Testomato API, this operation is `POST /project/:id/users` (base URL `https://testomato.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-user-to-project.md) for the provider-specific parameters and requirements.

