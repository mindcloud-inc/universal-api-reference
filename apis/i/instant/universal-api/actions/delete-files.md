# Instant: Delete Files

Deletes multiple files from Instant storage.

```
DELETE https://connect.mindcloud.co/v1/universal/instant/latest/actions/delete-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/instant/latest/actions/delete-files?connectionId=$CONNECTION_ID&filenames%5B%5D=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filenames[]": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instant/latest/actions/delete-files?${params}`, {
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
| `filenames[]` | array<string> | yes | Stored file paths to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Deleted file IDs returned by Instant. |

## Native endpoint

Through the native Instant API, this operation is `POST /admin/storage/files/delete` (base URL `https://api.instantdb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-files.md) for the provider-specific parameters and requirements.

