# Sage Sales Management: Login

Retrieves a session key from Sage Sales Management.

```
GET https://connect.mindcloud.co/v1/universal/sageSalesManagement/latest/actions/login
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sage Sales Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sageSalesManagement/latest/actions/login?connectionId=$CONNECTION_ID&username=%7B%7Bcredentials.publicKey%7D%7D&password=%7B%7Bcredentials.privateKey%7D%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "{{credentials.publicKey}}",
  "password": "{{credentials.privateKey}}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sageSalesManagement/latest/actions/login?${params}`, {
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
| `username` | string | yes | Public API key sent to the login endpoint as the username. Default: `{{credentials.publicKey}}`. |
| `password` | string | yes | Private API key sent to the login endpoint as the password. Default: `{{credentials.privateKey}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `token` | string | Session token |

## Native endpoint

Through the native Sage Sales Management API, this operation is `POST /login` (base URL `https://api.forcemanager.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/login.md) for the provider-specific parameters and requirements.

