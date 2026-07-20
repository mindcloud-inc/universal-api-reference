# DocumentPro: Delete Job

Deletes an extract job from DocumentPro.

```
DELETE https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/delete-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocumentPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/delete-job?connectionId=$CONNECTION_ID&request_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "request_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/delete-job?${params}`, {
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
| `request_id` | string | yes | The request_id of the extract job to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native DocumentPro API, this operation is `DELETE /files` (base URL `https://api.documentpro.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-job.md) for the provider-specific parameters and requirements.

