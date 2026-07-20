# Kadoa: Get Workflow Data



```
GET https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/get-workflow-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kadoa `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/get-workflow-data?connectionId=$CONNECTION_ID&workflowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/get-workflow-data?${params}`, {
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
| `workflowId` | string | yes | Workflow ID |
| `format` | list | no | Response format: json or csv One of: `csv`, `json`. Default: `json`. |
| `page` | number | no | Page number Default: `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `runId` | string | no | Specific run ID |
| `rowIds` | string | no | Filter output to specific row IDs. |
| `includeAnomalies` | boolean | no | Include anomalies in response. |
| `gzip` | boolean | no | Return gzip-compressed payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "executedAt": "2026-05-07T12:00:00.000Z",
      "pagination": {
        "limit": 1,
        "page": 1,
        "totalCount": 1,
        "totalPages": 1
      },
      "runId": "string",
      "workflowId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Extracted workflow rows. |
| `executedAt` | date | Run execution timestamp when available. |
| `pagination.limit` | number | Requested page size. |
| `pagination.page` | number | Current page number. |
| `pagination.totalCount` | number | Total rows available. |
| `pagination.totalPages` | number | Total pages. |
| `runId` | string | Workflow run identifier when available. |
| `workflowId` | string | Workflow identifier. |

## Native endpoint

Through the native Kadoa API, this operation is `GET /v4/workflows/:workflowId/data` (base URL `https://api.kadoa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflow-data.md) for the provider-specific parameters and requirements.

