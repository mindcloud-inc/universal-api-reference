# Camio: Get Settings

Retrieves settings from Camio.

```
GET https://connect.mindcloud.co/v1/universal/camio/latest/actions/get-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Camio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/camio/latest/actions/get-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/camio/latest/actions/get-settings?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "audioThreshold": 1,
      "notifications": {},
      "uploadToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audioThreshold` | number | The Camio audio threshold. |
| `notifications` | object | Notification settings keyed by notification type. |
| `uploadToken` | string | The user's upload token. |

## Native endpoint

Through the native Camio API, this operation is `GET /users/:user/settings` (base URL `https://camio.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-settings.md) for the provider-specific parameters and requirements.

