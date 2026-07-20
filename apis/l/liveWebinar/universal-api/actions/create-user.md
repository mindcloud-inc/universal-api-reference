# LiveWebinar: Create User

Creates a new user in LiveWebinar.

```
POST https://connect.mindcloud.co/v1/universal/liveWebinar/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LiveWebinar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/liveWebinar/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "password": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/liveWebinar/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "password": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `confirmed` | string | no |  |
| `countryCodeIso2` | string | no |  |
| `countryStateIso2` | string | no |  |
| `createdIp` | string | no |  |
| `dataLocation` | string | no |  |
| `email` | string | yes |  |
| `packageId` | string | no |  |
| `password` | string | yes |  |
| `status` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LiveWebinar API returns.

## Native endpoint

Through the native LiveWebinar API, this operation is `POST api/users` (base URL `https://api.archiebot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

