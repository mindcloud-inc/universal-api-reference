# Zoho Recruit: Get Bulk Read Job Details

Retrieves bulk read job details from Zoho Recruit.

```
GET https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/get-bulk-read-job-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Recruit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/get-bulk-read-job-details?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/get-bulk-read-job-details?${params}`, {
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
| `jobId` | string | yes | The unique ID of the bulk-read job. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callback": {},
      "createdBy": {},
      "createdTime": "string",
      "fileType": "string",
      "id": "string",
      "operation": "string",
      "query": {},
      "result": {},
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callback` | object |  |
| `createdBy` | object |  |
| `createdTime` | string |  |
| `fileType` | string |  |
| `id` | string |  |
| `operation` | string |  |
| `query` | object |  |
| `result` | object |  |
| `state` | string |  |

## Native endpoint

Through the native Zoho Recruit API, this operation is `GET https://recruit.zoho.com/recruit/bulk/v2/read/:jobId` (base URL `https://recruit.zoho.com/recruit/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bulk-read-job-details.md) for the provider-specific parameters and requirements.

