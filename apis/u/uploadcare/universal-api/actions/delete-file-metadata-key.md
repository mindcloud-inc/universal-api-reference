# Uploadcare: Delete File Metadata Key

Deletes a file metadata key from Uploadcare.

```
DELETE https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/delete-file-metadata-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uploadcare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/delete-file-metadata-key?connectionId=$CONNECTION_ID&key=string&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "string",
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/delete-file-metadata-key?${params}`, {
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
| `key` | string | yes | Metadata key name. |
| `uuid` | string | yes | Uploadcare file UUID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Uploadcare API returns.

## Native endpoint

Through the native Uploadcare API, this operation is `DELETE /files/:uuid/metadata/:key/` (base URL `https://api.uploadcare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-file-metadata-key.md) for the provider-specific parameters and requirements.

