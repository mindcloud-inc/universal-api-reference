# Dashly: Get User

Retrieves a Dashly user by identifier.

```
GET https://connect.mindcloud.co/v1/universal/dashly/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dashly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashly/latest/actions/get-user?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dashly/latest/actions/get-user?${params}`, {
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
| `id` | string | yes | Dashly ID or your external User ID. |
| `byUserId` | boolean | no | Interpret the identifier as your external User ID. Default: `true`. |
| `idAsString` | boolean | no | Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "app": 1,
      "id": 1,
      "mapUrl": {},
      "presence": "string",
      "props": {
        "$lastSeen": "string",
        "$name": "Ava Chen",
        "$namePlaceholder": "Ava Chen",
        "$score": 1,
        "$sessions": 1,
        "$userId": "string"
      },
      "removed": {},
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `app` | number |  |
| `id` | number |  |
| `mapUrl` | object |  |
| `presence` | string |  |
| `props.$lastSeen` | string |  |
| `props.$name` | string |  |
| `props.$namePlaceholder` | string |  |
| `props.$score` | number |  |
| `props.$sessions` | number |  |
| `props.$userId` | string |  |
| `removed` | object |  |
| `userId` | string |  |

## Native endpoint

Through the native Dashly API, this operation is `GET users/:id` (base URL `https://api.dashly.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

