# Zoho Analytics: Get Export Job Details

Retrieves export job details from Zoho Analytics.

```
GET https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/get-export-job-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/get-export-job-details?connectionId=$CONNECTION_ID&workspaceId=string&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/get-export-job-details?${params}`, {
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
| `workspaceId` | string | yes | ID of the workspace that owns the export job. |
| `jobId` | string | yes | ID of the export job to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "downloadUrl": "https://example.com",
        "expiryTime": "string",
        "jobCode": "string",
        "jobId": "string",
        "jobStatus": "string"
      },
      "status": "string",
      "summary": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.downloadUrl` | string |  |
| `data.expiryTime` | string |  |
| `data.jobCode` | string |  |
| `data.jobId` | string |  |
| `data.jobStatus` | string |  |
| `status` | string |  |
| `summary` | string |  |

## Native endpoint

Through the native Zoho Analytics API, this operation is `GET /bulk/workspaces/[:workspace-id]/exportjobs/[:job-id]` (base URL `https://analyticsapi.zoho.com/restapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-export-job-details.md) for the provider-specific parameters and requirements.

