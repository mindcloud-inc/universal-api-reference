# Neon: Delete database

Deletes a database from Neon.

```
DELETE https://connect.mindcloud.co/v1/universal/neon/latest/actions/delete-project-branch-database
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/neon/latest/actions/delete-project-branch-database?connectionId=$CONNECTION_ID&project_id=string&branch_id=string&database_name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string",
  "branch_id": "string",
  "database_name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/delete-project-branch-database?${params}`, {
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
| `project_id` | string | yes | Neon API parameter project_id |
| `branch_id` | string | yes | Neon API parameter branch_id |
| `database_name` | string | yes | Neon API parameter database_name |

## Response

```json
{
  "success": true,
  "data": [
    {
      "database": {},
      "operations": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `database` | object |  |
| `operations` | array<object> |  |

## Native endpoint

Through the native Neon API, this operation is `DELETE /projects/:project_id/branches/:branch_id/databases/:database_name` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-project-branch-database.md) for the provider-specific parameters and requirements.

