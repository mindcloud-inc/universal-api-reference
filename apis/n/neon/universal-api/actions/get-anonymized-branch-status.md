# Neon: Get anonymized branch status

Retrieves anonymized branch status from Neon.

```
GET https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-anonymized-branch-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-anonymized-branch-status?connectionId=$CONNECTION_ID&project_id=string&branch_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string",
  "branch_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/get-anonymized-branch-status?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "branch_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "failed_at": "2026-05-07T12:00:00.000Z",
      "last_run": {},
      "project_id": "string",
      "state": "string",
      "status_message": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branch_id` | string |  |
| `created_at` | date |  |
| `failed_at` | date |  |
| `last_run` | object |  |
| `project_id` | string |  |
| `state` | string |  |
| `status_message` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Neon API, this operation is `GET /projects/:project_id/branches/:branch_id/anonymized_status` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-anonymized-branch-status.md) for the provider-specific parameters and requirements.

