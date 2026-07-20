# gyfti: Add or Update Store User

Adds or updates a user in gyfti Store.

```
PUT https://connect.mindcloud.co/v1/universal/gyfti/latest/actions/add-or-update-store-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a gyfti `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gyfti/latest/actions/add-or-update-store-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userFirstname": "Ava",
  "userLastname": "Chen",
  "userEmail": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gyfti/latest/actions/add-or-update-store-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userFirstname": "Ava",
    "userLastname": "Chen",
    "userEmail": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userFirstname` | string | yes | Store user's first name. |
| `userLastname` | string | yes | Store user's last name. |
| `userEmail` | string | yes | Store user's email address. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userPool` | number | no | Optional initial pool amount when creating the store user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | object |  |
| `status` | string |  |

## Native endpoint

Through the native gyfti API, this operation is `POST /wf/add-user-store` (base URL `https://app.gyfti.fr/api/1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-or-update-store-user.md) for the provider-specific parameters and requirements.

