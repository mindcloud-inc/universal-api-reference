# Google Chat: Find Direct Message

Finds an existing Google Chat direct message with a user.

```
GET https://connect.mindcloud.co/v1/universal/googleChat/latest/actions/find-direct-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleChat/latest/actions/find-direct-message?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleChat/latest/actions/find-direct-message?${params}`, {
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
| `name` | string | yes | Enter the user's email address or Google Chat user ID. MindCloud will send it to Google as users/{value}. You can also paste a full users/... value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessSettings": {},
      "createTime": "2026-05-07T12:00:00.000Z",
      "customer": "string",
      "displayName": "Ava Chen",
      "lastActiveTime": "2026-05-07T12:00:00.000Z",
      "membershipCount": {},
      "name": "Ava Chen",
      "spaceHistoryState": "string",
      "spaceThreadingState": "string",
      "spaceType": "string",
      "spaceUri": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessSettings` | object |  |
| `createTime` | date |  |
| `customer` | string |  |
| `displayName` | string |  |
| `lastActiveTime` | date |  |
| `membershipCount` | object |  |
| `name` | string |  |
| `spaceHistoryState` | string |  |
| `spaceThreadingState` | string |  |
| `spaceType` | string |  |
| `spaceUri` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Google Chat API, this operation is `GET /spaces\:findDirectMessage` (base URL `https://chat.googleapis.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-direct-message.md) for the provider-specific parameters and requirements.

