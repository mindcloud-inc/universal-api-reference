# Range: Get User

Retrieve a user by its Range user ID.

```
GET https://connect.mindcloud.co/v1/universal/range/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Range `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/range/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/range/latest/actions/get-user?${params}`, {
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
| `userId` | string | no | The Range user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "absenceStatus": 1,
      "createdAt": "string",
      "currentAbsence": {},
      "internalState": {},
      "lastUpdatePublishedAt": "string",
      "orgId": "string",
      "profile": {},
      "settings": {},
      "state": {},
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `absenceStatus` | number |  |
| `createdAt` | string |  |
| `currentAbsence` | object |  |
| `internalState` | object |  |
| `lastUpdatePublishedAt` | string |  |
| `orgId` | string |  |
| `profile` | object |  |
| `settings` | object |  |
| `state` | object |  |
| `userId` | string |  |

## Native endpoint

Through the native Range API, this operation is `GET /v1/users/:userId` (base URL `https://api.range.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

