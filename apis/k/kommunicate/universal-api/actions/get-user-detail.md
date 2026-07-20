# Kommunicate: Get User Detail

Retrieves user details from Kommunicate.

```
GET https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/get-user-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kommunicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/get-user-detail?connectionId=$CONNECTION_ID&userIdList%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userIdList[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kommunicate/latest/actions/get-user-detail?${params}`, {
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
| `userIdList[]` | array<string> | yes | List of Kommunicate user IDs to retrieve. |
| `fetchLatestMessageTime` | boolean | no | Include each user's latest message timestamp in the response when true. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "connected": true,
      "createdAtTime": 1,
      "deactivated": true,
      "displayName": "Ava Chen",
      "lastMessageAtTime": 1,
      "metadata": {},
      "roleType": 1,
      "unreadCount": 1,
      "userId": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `connected` | boolean |  |
| `createdAtTime` | number |  |
| `deactivated` | boolean |  |
| `displayName` | string |  |
| `lastMessageAtTime` | number |  |
| `metadata` | object |  |
| `roleType` | number |  |
| `unreadCount` | number |  |
| `userId` | string |  |
| `userName` | string |  |

## Native endpoint

Through the native Kommunicate API, this operation is `POST /rest/ws/user/v2/detail` (base URL `https://services.kommunicate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-detail.md) for the provider-specific parameters and requirements.

