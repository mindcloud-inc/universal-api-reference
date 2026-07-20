# SparrowDesk: Get Bulk Job Status

Retrieves bulk job status from SparrowDesk.

```
GET https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/get-bulk-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparrowDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/get-bulk-job-status?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/get-bulk-job-status?${params}`, {
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
| `jobId` | string | yes | Bulk job ID returned by Bulk Create Contacts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactsCreated": 1,
      "contactsFailed": 1,
      "contactsUpdated": 1,
      "failedContacts": [
        {}
      ],
      "status": "string",
      "totalContacts": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactsCreated` | number | Number of contacts created. |
| `contactsFailed` | number | Number of contacts that failed. |
| `contactsUpdated` | number | Number of contacts updated. |
| `failedContacts` | array<object> | Failed contacts with error details. |
| `status` | string | Bulk job status. |
| `totalContacts` | number | Total contacts processed in the job. |

## Native endpoint

Through the native SparrowDesk API, this operation is `GET /bulk/status/{{jobId}}` (base URL `https://api.sparrowdesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bulk-job-status.md) for the provider-specific parameters and requirements.

