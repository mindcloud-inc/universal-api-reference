# Intruder: List Target Authentications



```
GET https://connect.mindcloud.co/v1/universal/intruder/latest/actions/list-target-authentications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intruder `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intruder/latest/actions/list-target-authentications?connectionId=$CONNECTION_ID&limit=25&offset=0&targetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "targetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intruder/latest/actions/list-target-authentications?${params}`, {
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

Through the native Intruder API, this operation is `GET /targets/:target_id/authentications/` (base URL `https://api.intruder.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-target-authentications.md) for the provider-specific parameters and requirements.

