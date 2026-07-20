# Element: Get Presence Status

Retrieves a user's presence status from Element.

```
GET https://connect.mindcloud.co/v1/universal/element/latest/actions/get-presence-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Element `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/element/latest/actions/get-presence-status?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/element/latest/actions/get-presence-status?${params}`, {
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
| `userId` | string | yes | Matrix user ID to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "presence": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `presence` | string |  |

## Native endpoint

Through the native Element API, this operation is `GET /_matrix/client/v3/presence/:userId/status` (base URL `{{credentials.homeserverUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-presence-status.md) for the provider-specific parameters and requirements.

