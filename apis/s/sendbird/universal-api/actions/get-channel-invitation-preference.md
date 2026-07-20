# Sendbird: Get Channel Invitation Preference



```
GET https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/get-channel-invitation-preference
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendbird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/get-channel-invitation-preference?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendbird/latest/actions/get-channel-invitation-preference?${params}`, {
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
| `userId` | string | yes | The user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autoAccept": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoAccept` | boolean |  |

## Native endpoint

Through the native Sendbird API, this operation is `GET /users/:userId/channel_invitation_preference` (base URL `https://api-{{credentials.applicationId}}.sendbird.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel-invitation-preference.md) for the provider-specific parameters and requirements.

