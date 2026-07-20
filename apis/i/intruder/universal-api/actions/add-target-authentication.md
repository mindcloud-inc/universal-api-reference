# Intruder: Add Target Authentication



```
POST https://connect.mindcloud.co/v1/universal/intruder/latest/actions/add-target-authentication
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intruder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intruder/latest/actions/add-target-authentication" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetId": "string",
  "name": "Ava Chen",
  "url": "https://example.com",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intruder/latest/actions/add-target-authentication', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetId": "string",
    "name": "Ava Chen",
    "url": "https://example.com",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recordedLoginFile` | string | no | Base64 data URI for a recorded login JSON file when type is recorded. |
| `targetId` | string | yes | The Intruder target identifier. |
| `name` | string | yes | A label for the target authentication. |
| `url` | string | yes | The authenticated URL or login page used by the target authentication. |
| `type` | string | yes | The Intruder authentication type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "csrfTokenField": "string",
      "enabled": true,
      "id": 1,
      "isAjaxSpiderEnabled": true,
      "loggedInIndicator": "string",
      "loginFormUrl": "https://example.com",
      "loginUrl": "https://example.com",
      "logoutUrl": "https://example.com",
      "name": "Ava Chen",
      "passwordField": "string",
      "realm": "string",
      "recordedLoginFile": "string",
      "type": "string",
      "url": "https://example.com",
      "usernameField": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `csrfTokenField` | string |  |
| `enabled` | boolean |  |
| `id` | number |  |
| `isAjaxSpiderEnabled` | boolean |  |
| `loggedInIndicator` | string |  |
| `loginFormUrl` | string |  |
| `loginUrl` | string |  |
| `logoutUrl` | string |  |
| `name` | string |  |
| `passwordField` | string |  |
| `realm` | string |  |
| `recordedLoginFile` | string |  |
| `type` | string |  |
| `url` | string |  |
| `usernameField` | string |  |

## Native endpoint

Through the native Intruder API, this operation is `POST /targets/:target_id/authentications/` (base URL `https://api.intruder.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-target-authentication.md) for the provider-specific parameters and requirements.

