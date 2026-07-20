# Appwrite: Create user target

Creates a new user target in your Appwrite project.

```
POST https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-create-target
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-create-target" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string",
  "targetId": "string",
  "providerType": "string",
  "identifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-create-target', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string",
    "targetId": "string",
    "providerType": "string",
    "identifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | User ID. |
| `targetId` | string | yes | Target ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `providerType` | string | yes | The target provider type. Can be one of the following: `email`, `sms` or `push`. |
| `identifier` | string | yes | The target identifier (token, email, phone etc.) |
| `providerId` | string | no | Provider ID. Message will be sent to this target from the specified provider ID. If no provider ID is set the first setup provider will be used. |
| `name` | string | no | Target name. Max length: 128 chars. For example: My Awesome App Galaxy S23. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$id": "string",
      "$updatedAt": "string",
      "expired": true,
      "identifier": "string",
      "name": "Ava Chen",
      "providerId": "string",
      "providerType": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$createdAt` | string | Target creation time in ISO 8601 format. |
| `$id` | string | Target ID. |
| `$updatedAt` | string | Target update date in ISO 8601 format. |
| `expired` | boolean | Is the target expired. |
| `identifier` | string | The target identifier. |
| `name` | string | Target Name. |
| `providerId` | string | Provider ID. |
| `providerType` | string | The target provider type. Can be one of the following: `email`, `sms` or `push`. |
| `userId` | string | User ID. |

## Native endpoint

Through the native Appwrite API, this operation is `POST /users/{userId}/targets` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/users-create-target.md) for the provider-specific parameters and requirements.

