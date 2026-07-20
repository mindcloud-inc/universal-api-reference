# DocRaptor: Get Async Document Status

Retrieves async document job status from DocRaptor.

```
GET https://connect.mindcloud.co/v1/universal/docRaptor/latest/actions/get-async-document-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocRaptor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docRaptor/latest/actions/get-async-document-status?connectionId=$CONNECTION_ID&statusId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "statusId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docRaptor/latest/actions/get-async-document-status?${params}`, {
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
| `statusId` | string | yes | Status ID returned by a DocRaptor async document creation request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "download_id": "string",
      "download_url": "https://example.com",
      "message": "string",
      "number_of_pages": 1,
      "status": "string",
      "validation_errors": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `download_id` | string | Document download ID returned when the async job is completed. |
| `download_url` | string | Document download URL returned when the async job is completed. |
| `message` | string | Completion or status message returned by DocRaptor when present. |
| `number_of_pages` | number | Number of pages in the completed PDF document when available. |
| `status` | string | Current async job status, such as queued, working, completed, or failed. |
| `validation_errors` | string | Validation error details returned when the async job fails. |

## Native endpoint

Through the native DocRaptor API, this operation is `GET https://docraptor.com/status/:status_id` (base URL `https://api.docraptor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-async-document-status.md) for the provider-specific parameters and requirements.

