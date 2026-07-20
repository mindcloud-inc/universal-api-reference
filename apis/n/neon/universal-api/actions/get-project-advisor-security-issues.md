# Neon: Get advisor issues

Retrieves advisor issues for a project from Neon.

```
GET https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-project-advisor-security-issues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-project-advisor-security-issues?connectionId=$CONNECTION_ID&project_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-project-advisor-security-issues?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `branch_id` | string | no | Neon API parameter branch_id |
| `database_name` | string | no | Neon API parameter database_name |
| `category` | list | no | Neon API parameter category One of: `0`, `1`. |
| `min_severity` | list | no | Neon API parameter min_severity One of: `0`, `1`, `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "issues": [
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
| `issues` | array<object> |  |

## Native endpoint

Through the native Neon API, this operation is `GET /projects/:project_id/advisors` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-advisor-security-issues.md) for the provider-specific parameters and requirements.

