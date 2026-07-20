# Communi App: Get User



```
GET https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Communi App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/get-user?connectionId=$CONNECTION_ID&id=343753" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "343753"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/get-user?${params}`, {
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
| `id` | number | yes | Default: `343753`. |

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

Through the native Communi App API, this operation is `GET /rest/user/:id` (base URL `https://api.communiapp.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

