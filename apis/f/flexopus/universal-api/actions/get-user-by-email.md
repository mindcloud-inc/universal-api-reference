# Flexopus: Get User by Email

Retrieves a Flexopus user by email address.

```
GET https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/get-user-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexopus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/get-user-by-email?connectionId=$CONNECTION_ID&userEmail=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userEmail": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/get-user-by-email?${params}`, {
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
| `userEmail` | string | yes | The email address of the user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "email": "ava@example.com",
        "extensionAttributes": {},
        "id": 1,
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.email` | string |  |
| `data.extensionAttributes` | object |  |
| `data.id` | number |  |
| `data.name` | string |  |

## Native endpoint

Through the native Flexopus API, this operation is `GET /users/by-email/:user_email` (base URL `{{credentials.tenantBaseUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-by-email.md) for the provider-specific parameters and requirements.

