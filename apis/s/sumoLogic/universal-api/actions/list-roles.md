# Sumo Logic: List Roles

Retrieves roles from your Sumo Logic organization.

```
GET https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumo Logic `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-roles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-roles?${params}`, {
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
| `name` | string | no | Only return roles matching the given name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autofillDependencies": true,
      "capabilities": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "description": "string",
      "filterPredicate": "string",
      "id": "string",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "modifiedBy": "string",
      "name": "Ava Chen",
      "systemDefined": true,
      "users": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autofillDependencies` | boolean |  |
| `capabilities[]` | string |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `description` | string |  |
| `filterPredicate` | string |  |
| `id` | string |  |
| `modifiedAt` | date |  |
| `modifiedBy` | string |  |
| `name` | string |  |
| `systemDefined` | boolean |  |
| `users[]` | string |  |

## Native endpoint

Through the native Sumo Logic API, this operation is `GET /v1/roles` (base URL `https://api.sumologic.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-roles.md) for the provider-specific parameters and requirements.

