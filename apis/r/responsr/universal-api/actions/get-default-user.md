# Responsr: Get Default User



```
GET https://connect.mindcloud.co/v1/universal/responsr/latest/actions/get-default-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Responsr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/responsr/latest/actions/get-default-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/responsr/latest/actions/get-default-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "firstName": "Ava",
      "groups": [
        {}
      ],
      "lastName": "Chen",
      "preferredLanguageId": 1,
      "projectParticipation": [
        {}
      ],
      "role": "string",
      "useBrowserLanguage": true,
      "useExtendedSession": true,
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `firstName` | string |  |
| `groups` | array<object> |  |
| `lastName` | string |  |
| `preferredLanguageId` | number |  |
| `projectParticipation` | array<object> |  |
| `role` | string |  |
| `useBrowserLanguage` | boolean |  |
| `useExtendedSession` | boolean |  |
| `userName` | string |  |

## Native endpoint

Through the native Responsr API, this operation is `GET /api/v1.0/users/default` (base URL `https://app.responsr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-default-user.md) for the provider-specific parameters and requirements.

