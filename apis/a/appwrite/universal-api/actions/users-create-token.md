# Appwrite: Create token

Creates a new token in your Appwrite project.

```
POST https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-create-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-create-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-create-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | User ID. |
| `length` | number | no | Token length in characters. The default length is 6 characters |
| `expire` | number | no | Token expiration period in seconds. The default expiration is 15 minutes. |

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

Through the native Appwrite API, this operation is `POST /users/{userId}/tokens` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/users-create-token.md) for the provider-specific parameters and requirements.

