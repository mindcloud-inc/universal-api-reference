# File.io: Delete File

Deletes a file from File.io by key.

```
DELETE https://connect.mindcloud.co/v1/universal/fileio/latest/actions/delete-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a File.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/fileio/latest/actions/delete-file?connectionId=$CONNECTION_ID&key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fileio/latest/actions/delete-file?${params}`, {
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
| `key` | string | yes | File.io file key to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | number | Provider status code from File.io. |
| `success` | boolean | Whether File.io deleted the file. |

## Native endpoint

Through the native File.io API, this operation is `DELETE /{{key}}` (base URL `https://file.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-file.md) for the provider-specific parameters and requirements.

