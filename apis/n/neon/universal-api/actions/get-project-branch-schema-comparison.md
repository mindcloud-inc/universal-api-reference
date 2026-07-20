# Neon: Compare database schema

Compares database schemas in Neon.

```
GET https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-project-branch-schema-comparison
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-project-branch-schema-comparison?connectionId=$CONNECTION_ID&project_id=string&branch_id=string&db_name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string",
  "branch_id": "string",
  "db_name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-project-branch-schema-comparison?${params}`, {
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
| `db_name` | string | yes | Neon API parameter db_name |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `base_branch_id` | string | no | Neon API parameter base_branch_id |
| `lsn` | string | no | Neon API parameter lsn |
| `timestamp` | date | no | Neon API parameter timestamp |
| `base_lsn` | string | no | Neon API parameter base_lsn |
| `base_timestamp` | date | no | Neon API parameter base_timestamp |

## Response

```json
{
  "success": true,
  "data": [
    {
      "diff": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `diff` | string |  |

## Native endpoint

Through the native Neon API, this operation is `GET /projects/:project_id/branches/:branch_id/compare_schema` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-branch-schema-comparison.md) for the provider-specific parameters and requirements.

