# SeaX: Import Contacts

Imports contacts into SeaX from a CSV file.

```
POST https://connect.mindcloud.co/v1/universal/seaX/latest/actions/import-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/import-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seaX/latest/actions/import-contacts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "ended_at": "string",
      "enqueued_at": "string",
      "error_code": 1,
      "error_msg": "string",
      "error_parameters": {},
      "job_id": "string",
      "started_at": "string",
      "status": {},
      "timeout": 1,
      "updated_at": "string",
      "workspace_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `ended_at` | string |  |
| `enqueued_at` | string |  |
| `error_code` | number |  |
| `error_msg` | string |  |
| `error_parameters` | object |  |
| `job_id` | string |  |
| `started_at` | string |  |
| `status` | object |  |
| `timeout` | number |  |
| `updated_at` | string |  |
| `workspace_id` | string |  |

## Native endpoint

Through the native SeaX API, this operation is `POST /import_contacts` (base URL `https://seax.seasalt.ai/seax-api/api/v1/workspace/{{credentials.workspaceId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-contacts.md) for the provider-specific parameters and requirements.

