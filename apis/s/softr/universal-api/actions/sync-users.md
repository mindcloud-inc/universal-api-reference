# Softr: Sync Users



```
PUT https://connect.mindcloud.co/v1/universal/softr/latest/actions/sync-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Softr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/softr/latest/actions/sync-users" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/softr/latest/actions/sync-users', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emails[]` | array<string> | no | Target email addresses to sync. Leave blank to let Softr sync all users for the selected app domain. Example: `user1@example.com, user2@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emails": [
        "ava@example.com"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emails[]` | string |  |

## Native endpoint

Through the native Softr API, this operation is `POST https://studio-api.softr.io/v1/api/users/sync` (base URL `https://tables-api.softr.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sync-users.md) for the provider-specific parameters and requirements.

