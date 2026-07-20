# Yandex ID: Get Authenticated User



```
GET https://connect.mindcloud.co/v1/universal/yandexID/latest/actions/get-authenticated-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yandex ID `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yandexID/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yandexID/latest/actions/get-authenticated-user?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jwtSecret` | string | no | Optional shared secret for validating OpenID JWT responses when you request JWT format from Yandex. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "birthday": "string",
      "clientId": "string",
      "defaultAvatarId": "string",
      "defaultEmail": "ava@example.com",
      "displayName": "Ava Chen",
      "emails": [
        "ava@example.com"
      ],
      "firstName": "Ava",
      "id": "string",
      "isAvatarEmpty": true,
      "lastName": "Chen",
      "login": "string",
      "psuid": "string",
      "realName": "Ava Chen",
      "sex": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `birthday` | string |  |
| `clientId` | string |  |
| `defaultAvatarId` | string |  |
| `defaultEmail` | string |  |
| `displayName` | string |  |
| `emails` | array<string> |  |
| `firstName` | string |  |
| `id` | string |  |
| `isAvatarEmpty` | boolean |  |
| `lastName` | string |  |
| `login` | string |  |
| `psuid` | string |  |
| `realName` | string |  |
| `sex` | string |  |

## Native endpoint

Through the native Yandex ID API, this operation is `GET /info` (base URL `https://login.yandex.ru`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-authenticated-user.md) for the provider-specific parameters and requirements.

