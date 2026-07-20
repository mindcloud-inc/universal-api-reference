# Vapi: List Squads

Retrieves a list of squads from Vapi.

```
GET https://connect.mindcloud.co/v1/universal/vapi/latest/actions/list-squads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vapi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vapi/latest/actions/list-squads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vapi/latest/actions/list-squads?${params}`, {
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
| `limit` | number | no | This is the maximum number of items to return. Defaults to 100. |
| `createdAtGt` | string | no | This will return items where the createdAt is greater than the specified value. |
| `createdAtLt` | string | no | This will return items where the createdAt is less than the specified value. |
| `createdAtGe` | string | no | This will return items where the createdAt is greater than or equal to the specified value. |
| `createdAtLe` | string | no | This will return items where the createdAt is less than or equal to the specified value. |
| `updatedAtGt` | string | no | This will return items where the updatedAt is greater than the specified value. |
| `updatedAtLt` | string | no | This will return items where the updatedAt is less than the specified value. |
| `updatedAtGe` | string | no | This will return items where the updatedAt is greater than or equal to the specified value. |
| `updatedAtLe` | string | no | This will return items where the updatedAt is less than or equal to the specified value. |

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

Through the native Vapi API, this operation is `GET /squad` (base URL `https://api.vapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-squads.md) for the provider-specific parameters and requirements.

