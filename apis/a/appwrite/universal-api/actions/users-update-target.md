# Appwrite: Update user target

Updates the user target in your Appwrite project.

```
PUT https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-update-target
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-update-target" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string",
  "targetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-update-target', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string",
    "targetId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | User ID. |
| `targetId` | string | yes | Target ID. |
| `identifier` | string | no | The target identifier (token, email, phone etc.) |
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

Through the native Appwrite API, this operation is `PATCH /users/{userId}/targets/{targetId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/users-update-target.md) for the provider-specific parameters and requirements.

