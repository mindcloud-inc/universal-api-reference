# Vapi: Delete Session

Deletes an existing session from Vapi.

```
DELETE https://connect.mindcloud.co/v1/universal/vapi/latest/actions/delete-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vapi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/vapi/latest/actions/delete-session?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vapi/latest/actions/delete-session?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "artifact": {},
      "assistant": {},
      "assistantId": "string",
      "assistantOverrides": {},
      "cost": 1,
      "costs": [
        {}
      ],
      "createdAt": "string",
      "customer": {},
      "customerId": "string",
      "expirationSeconds": 1,
      "id": "string",
      "messages": [
        {}
      ],
      "name": "Ava Chen",
      "orgId": "string",
      "phoneNumber": {},
      "phoneNumberId": "string",
      "squad": {},
      "squadId": "string",
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `artifact` | object |  |
| `assistant` | object |  |
| `assistantId` | string | This is the ID of the assistant associated with this session. Use this when referencing an existing assistant. |
| `assistantOverrides` | object |  |
| `cost` | number | This is the cost of the session in USD. |
| `costs` | array<object> | These are the costs of individual components of the session in USD. |
| `createdAt` | string | This is the ISO 8601 timestamp indicating when the session was created. |
| `customer` | object |  |
| `customerId` | string | This is the customerId of the customer associated with this session. |
| `expirationSeconds` | number | Session expiration time in seconds. Defaults to 24 hours (86400 seconds) if not set. |
| `id` | string | This is the unique identifier for the session. |
| `messages` | array<object> | This is an array of chat messages in the session. |
| `name` | string | This is a user-defined name for the session. Maximum length is 40 characters. |
| `orgId` | string | This is the unique identifier for the organization that owns this session. |
| `phoneNumber` | object |  |
| `phoneNumberId` | string | This is the ID of the phone number associated with this session. |
| `squad` | object |  |
| `squadId` | string | This is the squad ID associated with this session. Use this when referencing an existing squad. |
| `status` | string | This is the current status of the session. Can be either 'active' or 'completed'. |
| `updatedAt` | string | This is the ISO 8601 timestamp indicating when the session was last updated. |

## Native endpoint

Through the native Vapi API, this operation is `DELETE /session/:id` (base URL `https://api.vapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-session.md) for the provider-specific parameters and requirements.

