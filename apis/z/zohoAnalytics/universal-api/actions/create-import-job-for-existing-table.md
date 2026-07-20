# Zoho Analytics: Create Import Job For Existing Table

Creates an import job for a Zoho Analytics table.

```
POST https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/create-import-job-for-existing-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/create-import-job-for-existing-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "viewId": "string",
  "config": "[object Object]",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/create-import-job-for-existing-table', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "viewId": "string",
    "config": "[object Object]",
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | yes | ID of the workspace containing the target table. |
| `viewId` | string | yes | ID of the existing table view that should receive the imported file. |
| `config` | string | yes | Required stringified JSON import-job configuration, such as importType, fileType, and autoIdentify. Example: `[object Object]`. |
| `file` | file | yes | File payload to import asynchronously. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "jobId": "string"
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
| `data.jobId` | string |  |
| `status` | string |  |
| `summary` | string |  |

## Native endpoint

Through the native Zoho Analytics API, this operation is `POST /bulk/workspaces/[:workspace-id]/views/[:view-id]/data` (base URL `https://analyticsapi.zoho.com/restapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-import-job-for-existing-table.md) for the provider-specific parameters and requirements.

