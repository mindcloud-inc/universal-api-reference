# Cogmento CRM: Get Current User



```
GET https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cogmento CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/get-current-user?${params}`, {
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
      "accountId": "string",
      "accountOwner": true,
      "createdAt": "string",
      "email": "ava@example.com",
      "facebookAuth": true,
      "firstName": "Ava",
      "google": true,
      "hasDocusign": true,
      "hasTemplates": true,
      "id": "string",
      "lastName": "Chen",
      "linkedinAuth": true,
      "oneSignalIds": [
        "string"
      ],
      "phoneVerified": true,
      "quickbooks": true,
      "security": {
        "groups": [
          "string"
        ],
        "permissions": [
          "string"
        ],
        "ssi": true
      },
      "settings": {
        "locale": "string"
      },
      "telephony": true,
      "timezone": "string",
      "twilioNumbers": [
        "string"
      ],
      "verifiedForCalls": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `accountOwner` | boolean |  |
| `createdAt` | string |  |
| `email` | string |  |
| `facebookAuth` | boolean |  |
| `firstName` | string |  |
| `google` | boolean |  |
| `hasDocusign` | boolean |  |
| `hasTemplates` | boolean |  |
| `id` | string |  |
| `lastName` | string |  |
| `linkedinAuth` | boolean |  |
| `oneSignalIds` | array<string> |  |
| `phoneVerified` | boolean |  |
| `quickbooks` | boolean |  |
| `security.groups` | array<string> |  |
| `security.permissions` | array<string> |  |
| `security.ssi` | boolean |  |
| `settings.locale` | string |  |
| `telephony` | boolean |  |
| `timezone` | string |  |
| `twilioNumbers` | array<string> |  |
| `verifiedForCalls` | boolean |  |

## Native endpoint

Through the native Cogmento CRM API, this operation is `GET /auth/user` (base URL `https://api.freecrm.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

