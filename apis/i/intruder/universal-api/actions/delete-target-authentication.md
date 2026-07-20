# Intruder: Delete Target Authentication



```
DELETE https://connect.mindcloud.co/v1/universal/intruder/latest/actions/delete-target-authentication
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intruder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/intruder/latest/actions/delete-target-authentication?connectionId=$CONNECTION_ID&targetId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "targetId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intruder/latest/actions/delete-target-authentication?${params}`, {
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
| `targetId` | string | yes | The Intruder target identifier. |
| `id` | string | yes | The Intruder target authentication identifier. |

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

Through the native Intruder API, this operation is `DELETE /targets/:target_id/authentications/:id/` (base URL `https://api.intruder.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-target-authentication.md) for the provider-specific parameters and requirements.

