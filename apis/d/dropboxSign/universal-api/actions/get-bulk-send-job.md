# Dropbox Sign: Get Bulk Send Job

Retrieves a bulk send job from Dropbox Sign by ID.

```
GET https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/get-bulk-send-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/get-bulk-send-job?connectionId=$CONNECTION_ID&bulk_send_job_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bulk_send_job_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/get-bulk-send-job?${params}`, {
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
| `bulk_send_job_id` | string | yes | The ID of the Bulk Send Job to retrieve. |
| `page` | number | no | Which page number of the Bulk Send Job to return. |
| `pageSize` | number | no | Number of objects to return per page. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dropbox Sign API returns.

## Native endpoint

Through the native Dropbox Sign API, this operation is `GET /bulk_send_job/:bulk_send_job_id` (base URL `https://api.hellosign.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bulk-send-job.md) for the provider-specific parameters and requirements.

