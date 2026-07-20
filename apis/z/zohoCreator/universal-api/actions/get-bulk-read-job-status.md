# Zoho Creator: Get Bulk Read Job Status

Retrieves the status of a Zoho Creator bulk read job.

```
GET https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/get-bulk-read-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Creator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/get-bulk-read-job-status?connectionId=$CONNECTION_ID&accountOwnerName=Ava%20Chen&appLinkName=https%3A%2F%2Fexample.com&jobId=string&reportLinkName=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountOwnerName": "Ava Chen",
  "appLinkName": "https://example.com",
  "jobId": "string",
  "reportLinkName": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/get-bulk-read-job-status?${params}`, {
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
| `accountOwnerName` | string | yes | Zoho Creator account owner name. |
| `appLinkName` | string | yes | Zoho Creator app link name. |
| `jobId` | string | yes | Zoho Creator bulk read job ID. |
| `reportLinkName` | string | yes | Zoho Creator report link name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "details": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Zoho Creator response code. |
| `details` | object | Bulk read job status details and download metadata. |

## Native endpoint

Through the native Zoho Creator API, this operation is `GET /bulk/:account_owner_name/:app_link_name/report/:report_link_name/read/:job_ID` (base URL `https://www.zohoapis.com/creator/v2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bulk-read-job-status.md) for the provider-specific parameters and requirements.

