# LastPass: Disable User

Disables an existing user in LastPass.

```
PUT https://connect.mindcloud.co/v1/universal/lastPass/latest/actions/disable-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LastPass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lastPass/latest/actions/disable-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lastPass/latest/actions/disable-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | The email address of the user to disable. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "success": true,
      "unchangedUsers": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |
| `success` | boolean |  |
| `unchangedUsers` | array<string> |  |

## Native endpoint

Through the native LastPass API, this operation is `POST /enterpriseapi.php` (base URL `https://lastpass.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/disable-user.md) for the provider-specific parameters and requirements.

