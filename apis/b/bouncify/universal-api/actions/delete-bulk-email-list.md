# Bouncify: Delete Bulk Email List

Deletes a bulk email list from Bouncify.

```
DELETE https://connect.mindcloud.co/v1/universal/bouncify/latest/actions/delete-bulk-email-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bouncify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/bouncify/latest/actions/delete-bulk-email-list?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bouncify/latest/actions/delete-bulk-email-list?${params}`, {
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
| `jobId` | string | yes | Bulk verification job id to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string | Bulk verification job identifier that was deleted. |
| `message` | string | Provider message describing the delete result. |
| `success` | boolean | Whether the delete request succeeded. |

## Native endpoint

Through the native Bouncify API, this operation is `DELETE /bulk/:job_id` (base URL `https://api.bouncify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-bulk-email-list.md) for the provider-specific parameters and requirements.

