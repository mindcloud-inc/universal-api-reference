# Sendbird: Check Group Channel Member



```
GET https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/check-group-channel-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendbird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/check-group-channel-member?connectionId=$CONNECTION_ID&channelUrl=https%3A%2F%2Fexample.com&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelUrl": "https://example.com",
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/check-group-channel-member?${params}`, {
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
| `channelUrl` | string | yes | The group channel URL. |
| `userId` | string | yes | The user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isActive": true,
      "nickname": "Ava Chen",
      "profileUrl": "https://example.com",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isActive` | boolean |  |
| `nickname` | string |  |
| `profileUrl` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Sendbird API, this operation is `GET /group_channels/:channelUrl/members/:userId` (base URL `https://api-{{credentials.applicationId}}.sendbird.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-group-channel-member.md) for the provider-specific parameters and requirements.

