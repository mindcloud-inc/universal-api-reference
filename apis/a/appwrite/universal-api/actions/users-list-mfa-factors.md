# Appwrite: List factors

Retrieves a list of factors from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-list-mfa-factors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-list-mfa-factors?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-list-mfa-factors?${params}`, {
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
| `userId` | string | yes | User ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": true,
      "phone": true,
      "recoveryCode": true,
      "totp": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | boolean | Can email be used for MFA challenge for this account. |
| `phone` | boolean | Can phone (SMS) be used for MFA challenge for this account. |
| `recoveryCode` | boolean | Can recovery code be used for MFA challenge for this account. |
| `totp` | boolean | Can TOTP be used for MFA challenge for this account. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /users/{userId}/mfa/factors` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/users-list-mfa-factors.md) for the provider-specific parameters and requirements.

