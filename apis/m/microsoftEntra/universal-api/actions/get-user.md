# Microsoft Entra: Get User



```
GET https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Entra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=87d349ed-44d7-43e1-9a83-5f2406dee5bd" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "87d349ed-44d7-43e1-9a83-5f2406dee5bd"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/get-user?${params}`, {
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
| `userId` | list<string> | yes | Example: `87d349ed-44d7-43e1-9a83-5f2406dee5bd`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `select` | string | no | Comma-separated properties, such as id,displayName. Example: `id,displayName`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayName": "Ava Chen",
      "givenName": "Ava",
      "id": "string",
      "jobTitle": "string",
      "mail": "ava@example.com",
      "mobilePhone": "string",
      "officeLocation": "string",
      "preferredLanguage": "string",
      "surname": "Chen",
      "userPrincipalName": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string |  |
| `givenName` | string |  |
| `id` | string |  |
| `jobTitle` | string |  |
| `mail` | string |  |
| `mobilePhone` | string |  |
| `officeLocation` | string |  |
| `preferredLanguage` | string |  |
| `surname` | string |  |
| `userPrincipalName` | string |  |

## Native endpoint

Through the native Microsoft Entra API, this operation is `GET /users/:userId` (base URL `https://graph.microsoft.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

