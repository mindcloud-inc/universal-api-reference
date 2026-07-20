# Appwrite: Update password recovery (confirmation)

Completes password recovery flow in Appwrite.

```
PUT https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/account-update-recovery
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/account-update-recovery" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string",
  "secret": "string",
  "password": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/account-update-recovery', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string",
    "secret": "string",
    "password": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | User ID. |
| `secret` | string | yes | Valid reset token. |
| `password` | string | yes | New user password. Must be between 8 and 256 chars. |

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

Through the native Appwrite API, this operation is `PUT /account/recovery` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/account-update-recovery.md) for the provider-specific parameters and requirements.

