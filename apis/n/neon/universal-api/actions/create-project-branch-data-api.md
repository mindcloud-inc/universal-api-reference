# Neon: Create Neon Data API

Creates Neon Data API configuration in Neon.

```
POST https://connect.mindcloud.co/v1/universal/neon/latest/actions/create-project-branch-data-api
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neon/latest/actions/create-project-branch-data-api" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "string",
  "branch_id": "string",
  "database_name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neon/latest/actions/create-project-branch-data-api', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "string",
    "branch_id": "string",
    "database_name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project_id` | string | yes | Neon API parameter project_id |
| `branch_id` | string | yes | Neon API parameter branch_id |
| `database_name` | string | yes | Neon API parameter database_name |
| `auth_provider` | list | no | Neon API parameter auth_provider One of: `0`, `1`. |
| `jwks_url` | string | no | Neon API parameter jwks_url |
| `provider_name` | string | no | Neon API parameter provider_name |
| `jwt_audience` | string | no | Neon API parameter jwt_audience |
| `add_default_grants` | boolean | no | Neon API parameter add_default_grants |
| `skip_auth_schema` | boolean | no | Neon API parameter skip_auth_schema |
| `settings` | object | no | Neon API parameter settings |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string |  |

## Native endpoint

Through the native Neon API, this operation is `POST /projects/:project_id/branches/:branch_id/data-api/:database_name` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-branch-data-api.md) for the provider-specific parameters and requirements.

