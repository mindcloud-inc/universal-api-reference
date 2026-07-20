# Appwrite: Get user target

Retrieves the user target from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-get-target
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-get-target?connectionId=$CONNECTION_ID&userId=string&targetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string",
  "targetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-get-target?${params}`, {
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
| `targetId` | string | yes | Target ID. |

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

Through the native Appwrite API, this operation is `GET /users/{userId}/targets/{targetId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/users-get-target.md) for the provider-specific parameters and requirements.

