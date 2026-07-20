# OpnForm: Check Submission Export Status

Retrieves submission export job status from OpnForm.

```
GET https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/check-submission-export-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpnForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/check-submission-export-status?connectionId=$CONNECTION_ID&id=1&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/check-submission-export-status?${params}`, {
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
| `id` | number | yes | The numeric ID of the form. |
| `jobId` | string | yes | The export job identifier returned by OpnForm for an asynchronous export. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "progress": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `progress` | number |  |
| `status` | string |  |

## Native endpoint

Through the native OpnForm API, this operation is `GET /open/forms/:id/submissions/export/status/:jobId` (base URL `https://api.opnform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-submission-export-status.md) for the provider-specific parameters and requirements.

