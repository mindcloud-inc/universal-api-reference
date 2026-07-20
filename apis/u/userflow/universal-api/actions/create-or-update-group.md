# Userflow: Create Or Update Group

Creates or updates a group in Userflow.

```
POST https://connect.mindcloud.co/v1/universal/userflow/latest/actions/create-or-update-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/userflow/latest/actions/create-or-update-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userflow/latest/actions/create-or-update-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Unique identifier for the group. |
| `attributes` | object | no | Group attributes to merge into the Userflow group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "name": "Ava Chen"
      },
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "memberships": {},
      "object": "string",
      "users": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Group attributes. |
| `attributes.name` | string | Group name. |
| `created_at` | date | Group creation timestamp. |
| `id` | string | Group ID. |
| `memberships` | object | Group memberships. |
| `object` | string | Returned object type. |
| `users` | object | Users in the group. |

## Native endpoint

Through the native Userflow API, this operation is `POST /groups` (base URL `https://api.userflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-group.md) for the provider-specific parameters and requirements.

