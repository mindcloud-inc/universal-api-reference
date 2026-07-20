# JustCall: Get a User

Retrieves a user from JustCall.

```
GET https://connect.mindcloud.co/v1/universal/justCall/latest/actions/get-a-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JustCall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/justCall/latest/actions/get-a-user?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/justCall/latest/actions/get-a-user?${params}`, {
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
| `id` | number | yes | The JustCall user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "available": "string",
      "createdAt": "string",
      "email": "ava@example.com",
      "extension": 1,
      "groups": [
        "string"
      ],
      "id": 1,
      "lastLoginTimestamp": "string",
      "name": "Ava Chen",
      "onCall": "string",
      "ownedNumbers": [
        "string"
      ],
      "role": "string",
      "sharedNumbers": [
        "string"
      ],
      "timezone": "string",
      "unavailabilityReason": "string",
      "workingHoursType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available` | string |  |
| `createdAt` | string |  |
| `email` | string |  |
| `extension` | number |  |
| `groups` | array<string> |  |
| `id` | number |  |
| `lastLoginTimestamp` | string |  |
| `name` | string |  |
| `onCall` | string |  |
| `ownedNumbers` | array<string> |  |
| `role` | string |  |
| `sharedNumbers` | array<string> |  |
| `timezone` | string |  |
| `unavailabilityReason` | string |  |
| `workingHoursType` | string |  |

## Native endpoint

Through the native JustCall API, this operation is `GET /v2.1/users/:id` (base URL `https://api.justcall.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-user.md) for the provider-specific parameters and requirements.

