# Neon: Start anonymization

Starts anonymization for a branch in Neon.

```
POST https://connect.mindcloud.co/v1/universal/neon/latest/actions/start-anonymization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neon/latest/actions/start-anonymization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "string",
  "branch_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neon/latest/actions/start-anonymization', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "string",
    "branch_id": "string"
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

Through the native Neon API, this operation is `POST /projects/:project_id/branches/:branch_id/anonymize` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-anonymization.md) for the provider-specific parameters and requirements.

