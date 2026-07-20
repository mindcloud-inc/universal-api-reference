# Docmosis: Get Upload Template Batch Status



```
GET https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/get-upload-template-batch-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docmosis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/get-upload-template-batch-status?connectionId=$CONNECTION_ID&userJobId=docmosis-s3-134628-b1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userJobId": "docmosis-s3-134628-b1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/get-upload-template-batch-status?${params}`, {
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
| `userJobId` | string | yes | Batch upload job identifier returned by Upload Template Batch. Example: `docmosis-s3-134628-b1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobStatus": {},
      "longMsg": "string",
      "shortMsg": "string",
      "succeeded": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobStatus` | object | Job status details for the batch upload. |
| `longMsg` | string | Detailed status message from Docmosis. |
| `shortMsg` | string | Short status message from Docmosis. |
| `succeeded` | boolean | Whether the batch status request succeeded. |

## Native endpoint

Through the native Docmosis API, this operation is `POST /uploadTemplateBatchStatus` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-upload-template-batch-status.md) for the provider-specific parameters and requirements.

