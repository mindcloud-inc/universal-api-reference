# ImageKit.io: Delete Multiple Files

Deletes multiple files from the ImageKit.io media library.

```
DELETE https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/delete-multiple-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ImageKit.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/delete-multiple-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imageKit/latest/actions/delete-multiple-files?${params}`, {
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
| `fileIds` | list<string> | no | Default: `["6995e3df5c7cd75eb84cddae"]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "successfullyDeletedFileIds": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `successfullyDeletedFileIds` | array<string> |  |

## Native endpoint

Through the native ImageKit.io API, this operation is `POST /files/batch/deleteByFileIds` (base URL `https://api.imagekit.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-multiple-files.md) for the provider-specific parameters and requirements.

