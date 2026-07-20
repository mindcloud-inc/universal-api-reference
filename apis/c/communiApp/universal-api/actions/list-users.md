# Communi App: List Users



```
GET https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Communi App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-users?connectionId=$CONNECTION_ID&communiApp=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "communiApp": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-users?${params}`, {
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
| `communiApp` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_loadStatus": 1,
      "_rls": 1,
      "avatarCode": "string",
      "careerAspiration": "string",
      "communiApp": 1,
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "lastNameInitial": "Chen",
      "ort": "string",
      "parish": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_loadStatus` | number |  |
| `_rls` | number |  |
| `avatarCode` | string |  |
| `careerAspiration` | string |  |
| `communiApp` | number |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `lastNameInitial` | string |  |
| `ort` | string |  |
| `parish` | string |  |

## Native endpoint

Through the native Communi App API, this operation is `GET /rest/user` (base URL `https://api.communiapp.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

