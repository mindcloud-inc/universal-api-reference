# Zoho Analytics: Download Exported Data

Downloads exported data from Zoho Analytics.

```
GET https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/download-exported-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/download-exported-data?connectionId=$CONNECTION_ID&workspaceId=string&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/download-exported-data?${params}`, {
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
| `jobId` | string | yes | ID of the completed export job to download. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho Analytics API returns.

## Native endpoint

Through the native Zoho Analytics API, this operation is `GET /bulk/workspaces/[:workspace-id]/exportjobs/[:job-id]/data` (base URL `https://analyticsapi.zoho.com/restapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-exported-data.md) for the provider-specific parameters and requirements.

