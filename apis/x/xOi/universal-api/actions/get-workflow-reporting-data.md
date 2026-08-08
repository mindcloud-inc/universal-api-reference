# XOi: Get Workflow Reporting Data



```
GET https://connect.mindcloud.co/v1/universal/xOi/latest/actions/get-workflow-reporting-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XOi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xOi/latest/actions/get-workflow-reporting-data?connectionId=$CONNECTION_ID&jobId=string&workflowJobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string",
  "workflowJobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xOi/latest/actions/get-workflow-reporting-data?${params}`, {
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
| `jobId` | string | yes |  |
| `workflowJobId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "string",
      "createdAt": "string",
      "jobId": "string",
      "jobLocation": "string",
      "orgId": "string",
      "reportingCategory": "string",
      "stepData": {},
      "workflowJobId": "string",
      "workflowName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | string |  |
| `createdAt` | string |  |
| `jobId` | string |  |
| `jobLocation` | string |  |
| `orgId` | string |  |
| `reportingCategory` | string |  |
| `stepData` | object |  |
| `workflowJobId` | string |  |
| `workflowName` | string |  |

## Native endpoint

Through the native XOi API, this operation is `GET https://api-jobs-external.xoi.io/prod/reporting-data/job/:jobId/workflow-job/:workflowJobId` (base URL `https://gql-jobs-external.xoi.io/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflow-reporting-data.md) for the provider-specific parameters and requirements.

