# Appwrite: Create MFA challenge

Creates a new MFA challenge in your Appwrite project.

```
POST https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/account-create-mfa-challenge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/account-create-mfa-challenge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "factor": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/account-create-mfa-challenge', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "factor": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `factor` | string | yes | Factor used for verification. Must be one of following: `email`, `phone`, `totp`, `recoveryCode`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$id": "string",
      "expire": "string",
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
| `userId` | string | User ID. |

## Native endpoint

Through the native Appwrite API, this operation is `POST /account/mfa/challenges` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/account-create-mfa-challenge.md) for the provider-specific parameters and requirements.

