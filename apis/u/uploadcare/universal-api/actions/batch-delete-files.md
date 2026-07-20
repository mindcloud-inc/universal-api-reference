# Uploadcare: Batch Delete Files

Deletes multiple files from Uploadcare storage.

```
DELETE https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/batch-delete-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uploadcare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/batch-delete-files?connectionId=$CONNECTION_ID&uuids%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuids[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/batch-delete-files?${params}`, {
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
| `uuids[]` | array<string> | yes | List of Uploadcare file UUIDs to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "problems": {},
      "result": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `problems` | object | Per-file problems returned by Uploadcare when present. |
| `result` | array<object> | Deleted file records returned by Uploadcare. |
| `status` | string | Batch operation status. |

## Native endpoint

Through the native Uploadcare API, this operation is `DELETE /files/storage/` (base URL `https://api.uploadcare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-delete-files.md) for the provider-specific parameters and requirements.

