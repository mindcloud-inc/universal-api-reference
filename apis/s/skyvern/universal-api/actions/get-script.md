# Skyvern: Get Script

Retrieves a script by ID from Skyvern.

```
GET https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/get-script
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skyvern `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/get-script?connectionId=$CONNECTION_ID&scriptId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scriptId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/get-script?${params}`, {
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
| `scriptId` | string | yes | The unique identifier of the script |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "modified_at": "2026-05-07T12:00:00.000Z",
      "organization_id": "string",
      "run_id": "string",
      "script_id": "string",
      "script_revision_id": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Script creation timestamp |
| `deleted_at` | date | Soft delete timestamp |
| `modified_at` | date | Script last modified timestamp |
| `organization_id` | string | Organization ID |
| `run_id` | string | Workflow or task run ID that generated the script |
| `script_id` | string | Stable script identifier |
| `script_revision_id` | string | Unique identifier for this script revision |
| `version` | number | Script version number |

## Native endpoint

Through the native Skyvern API, this operation is `GET /v1/scripts/:script_id` (base URL `https://api.skyvern.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-script.md) for the provider-specific parameters and requirements.

