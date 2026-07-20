# validTo: Delete Bulk Validation List

Deletes a bulk validation list from validTo.

```
DELETE https://connect.mindcloud.co/v1/universal/validTo/latest/actions/delete-bulk-validation-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a validTo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/validTo/latest/actions/delete-bulk-validation-list?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/validTo/latest/actions/delete-bulk-validation-list?${params}`, {
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
| `jobId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job_id": "string",
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
| `job_id` | string | The job_id corresponding to the list being deleted. |
| `message` | string | Describes the delete result. |
| `success` | boolean | Whether the API request call was successful. |

## Native endpoint

Through the native validTo API, this operation is `DELETE /bulk/:jobId` (base URL `https://api.validto.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-bulk-validation-list.md) for the provider-specific parameters and requirements.

