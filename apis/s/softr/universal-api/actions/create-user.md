# Softr: Create User



```
POST https://connect.mindcloud.co/v1/universal/softr/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Softr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/softr/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fullName": "John Richardson",
  "email": "john@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/softr/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fullName": "John Richardson",
    "email": "john@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fullName` | string | yes | Full name for the Softr user. Example: `John Richardson`. |
| `email` | string | yes | Email address for the Softr user. Example: `john@example.com`. |
| `password` | string | no | Password for the Softr user. Leave blank to let Softr generate one automatically. Example: `TempPassword123`. |
| `generateMagicLink` | boolean | no | Whether Softr should generate a magic link for the new user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "email": "ava@example.com",
      "fullName": "Ava Chen",
      "magicLink": "https://example.com",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string |  |
| `email` | string |  |
| `fullName` | string |  |
| `magicLink` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native Softr API, this operation is `POST https://studio-api.softr.io/v1/api/users` (base URL `https://tables-api.softr.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

