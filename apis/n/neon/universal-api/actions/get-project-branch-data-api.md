# Neon: Get Neon Data API

Retrieves Neon Data API configuration from Neon.

```
GET https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-project-branch-data-api
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-project-branch-data-api?connectionId=$CONNECTION_ID&project_id=string&branch_id=string&database_name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string",
  "branch_id": "string",
  "database_name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-project-branch-data-api?${params}`, {
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
      "available_schemas": [
        "string"
      ],
      "settings": {},
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available_schemas` | array<string> |  |
| `settings` | object |  |
| `status` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Neon API, this operation is `GET /projects/:project_id/branches/:branch_id/data-api/:database_name` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-branch-data-api.md) for the provider-specific parameters and requirements.

