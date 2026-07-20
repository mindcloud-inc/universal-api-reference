# Letta: Retrieve Run

Retrieves an existing run from Letta.

```
GET https://connect.mindcloud.co/v1/universal/letta/latest/actions/retrieve-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Letta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/letta/latest/actions/retrieve-run?connectionId=$CONNECTION_ID&runId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "runId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/letta/latest/actions/retrieve-run?${params}`, {
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
| `runId` | string | yes | The Letta run ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completed_at": "2026-05-07T12:00:00.000Z",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed_at` | date |  |
| `created_at` | date |  |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Letta API, this operation is `GET /v1/runs/:run_id` (base URL `https://api.letta.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-run.md) for the provider-specific parameters and requirements.

