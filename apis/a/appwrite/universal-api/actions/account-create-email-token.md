# Appwrite: Create email token (OTP)

Creates a new email token OTP in your Appwrite project.

```
POST https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/account-create-email-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/account-create-email-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/account-create-email-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | User ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. If the email address has never been used, a new account is created using the provided userId. Otherwise, if the email address is already attached to an account, the user ID is ignored. |
| `email` | string | yes | User email. |
| `phrase` | boolean | no | Toggle for security phrase. If enabled, email will be send with a randomly generated phrase and the phrase will also be included in the response. Confirming phrases match increases the security of your authentication flow. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$id": "string",
      "expire": "string",
      "phrase": "string",
      "secret": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$createdAt` | string | Token creation date in ISO 8601 format. |
| `$id` | string | Token ID. |
| `expire` | string | Token expiration date in ISO 8601 format. |
| `phrase` | string | Security phrase of a token. Empty if security phrase was not requested when creating a token. It includes randomly generated phrase which is also sent in the external resource such as email. |
| `secret` | string | Token secret key. This will return an empty string unless the response is returned using an API key or as part of a webhook payload. |
| `userId` | string | User ID. |

## Native endpoint

Through the native Appwrite API, this operation is `POST /account/tokens/email` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/account-create-email-token.md) for the provider-specific parameters and requirements.

