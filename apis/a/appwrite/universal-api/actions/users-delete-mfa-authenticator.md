# Appwrite: Delete authenticator

Deletes the authenticator from your Appwrite project.

```
DELETE https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-delete-mfa-authenticator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-delete-mfa-authenticator?connectionId=$CONNECTION_ID&userId=string&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string",
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-delete-mfa-authenticator?${params}`, {
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
| `type` | string | yes | Type of authenticator. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | True when the request succeeds. |

## Native endpoint

Through the native Appwrite API, this operation is `DELETE /users/{userId}/mfa/authenticators/{type}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/users-delete-mfa-authenticator.md) for the provider-specific parameters and requirements.

