# Eranol: Delete Job

Deletes an existing processing job from Eranol.

```
DELETE https://connect.mindcloud.co/v1/universal/eranol/latest/actions/delete-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eranol `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/eranol/latest/actions/delete-job?connectionId=$CONNECTION_ID&job_id=460719d5-d0ad-4fd8-a81c-ebc2435fbfaa" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "job_id": "460719d5-d0ad-4fd8-a81c-ebc2435fbfaa"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eranol/latest/actions/delete-job?${params}`, {
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
| `job_id` | string | yes | Job ID returned by an Eranol create action. Example: `460719d5-d0ad-4fd8-a81c-ebc2435fbfaa`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | string | Deleted Eranol job identifier. |

## Native endpoint

Through the native Eranol API, this operation is `DELETE /ffmpeg/jobs/:job_id` (base URL `https://eranol.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-job.md) for the provider-specific parameters and requirements.

