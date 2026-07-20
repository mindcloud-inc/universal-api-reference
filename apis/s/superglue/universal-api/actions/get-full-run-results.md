# Superglue: Get Full Run Results

Retrieves full run results from Superglue.

```
GET https://connect.mindcloud.co/v1/universal/superglue/latest/actions/get-full-run-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superglue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superglue/latest/actions/get-full-run-results?connectionId=$CONNECTION_ID&runId=7f3e9c1a-2b4d-4e8f-9a3b-1c5d7e9f2a4b" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "runId": "7f3e9c1a-2b4d-4e8f-9a3b-1c5d7e9f2a4b"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superglue/latest/actions/get-full-run-results?${params}`, {
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
| `runId` | string | yes | ID of the Superglue run. Example: `7f3e9c1a-2b4d-4e8f-9a3b-1c5d7e9f2a4b`. |
| `truncate` | list | no | If true, truncate large results for preview. One of: `false`, `true`. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "error": "string",
      "message": "string",
      "runId": "string",
      "stepResults": [
        {}
      ],
      "storedAt": "2026-05-07T12:00:00.000Z",
      "success": true,
      "toolPayload": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Full tool execution result data. |
| `error` | string | Error message for failed stored results. |
| `message` | string | Message returned when no stored results are available. |
| `runId` | string | Unique identifier for the run results. |
| `stepResults` | array<object> | Per-step execution results. |
| `storedAt` | date | Timestamp when the run results were stored. |
| `success` | boolean | Whether the stored run results were returned successfully. |
| `toolPayload` | object | Inputs provided when running the tool. |

## Native endpoint

Through the native Superglue API, this operation is `GET /runs/:runId/results` (base URL `https://api.superglue.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-full-run-results.md) for the provider-specific parameters and requirements.

