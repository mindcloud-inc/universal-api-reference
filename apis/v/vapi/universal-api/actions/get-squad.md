# Vapi: Get Squad

Retrieves a squad from Vapi by ID.

```
GET https://connect.mindcloud.co/v1/universal/vapi/latest/actions/get-squad
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vapi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vapi/latest/actions/get-squad?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vapi/latest/actions/get-squad?${params}`, {
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
      "createdAt": "string",
      "id": "string",
      "members": [
        {}
      ],
      "membersOverrides": {},
      "name": "Ava Chen",
      "orgId": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | This is the ISO 8601 date-time string of when the squad was created. |
| `id` | string | This is the unique identifier for the squad. |
| `members` | array<object> | This is the list of assistants that make up the squad.  The call will start with the first assistant in the list. |
| `membersOverrides` | object |  |
| `name` | string | This is the name of the squad. |
| `orgId` | string | This is the unique identifier for the org that this squad belongs to. |
| `updatedAt` | string | This is the ISO 8601 date-time string of when the squad was last updated. |

## Native endpoint

Through the native Vapi API, this operation is `GET /squad/:id` (base URL `https://api.vapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-squad.md) for the provider-specific parameters and requirements.

