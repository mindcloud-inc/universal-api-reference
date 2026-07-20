# Wistia: Show Background Job Status

Retrieves the status of a Wistia background job.

```
GET https://connect.mindcloud.co/v1/universal/wistia/latest/actions/show-background-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wistia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wistia/latest/actions/show-background-job-status?connectionId=$CONNECTION_ID&backgroundJobStatusId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "backgroundJobStatusId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wistia/latest/actions/show-background-job-status?${params}`, {
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
| `backgroundJobStatusId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "backgroundJobStatus": {
        "id": 1,
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backgroundJobStatus` | object | A background job keeps track of the progress of an asynchronous task, e.g bulk archiving media, translating media, etc. |
| `backgroundJobStatus.id` | number | The ID of the background job that's been queued for the request. |
| `backgroundJobStatus.status` | string | The status of the background job that's been queued for the request. |

## Native endpoint

Through the native Wistia API, this operation is `GET /modern/background_job_status/:backgroundJobStatusId` (base URL `https://api.wistia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/show-background-job-status.md) for the provider-specific parameters and requirements.

