# Skyvern: Get Run Timeline

Retrieves timeline events for a run from Skyvern.

```
GET https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/get-run-timeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skyvern `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/get-run-timeline?connectionId=$CONNECTION_ID&runId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "runId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skyvern/latest/actions/get-run-timeline?${params}`, {
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
| `runId` | string | yes | The workflow run or task run ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "block": {},
      "children": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "thought": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `block` | object | Timeline block payload |
| `children` | array<object> | Child timeline entries |
| `createdAt` | date | Timeline entry creation timestamp |
| `modifiedAt` | date | Timeline entry last modification timestamp |
| `thought` | object | Timeline thought payload |
| `type` | string | Timeline entry type |

## Native endpoint

Through the native Skyvern API, this operation is `GET /v1/runs/:run_id/timeline` (base URL `https://api.skyvern.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-run-timeline.md) for the provider-specific parameters and requirements.

