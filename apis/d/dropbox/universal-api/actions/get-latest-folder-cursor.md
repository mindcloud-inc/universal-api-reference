# Dropbox: Get Latest Folder Cursor

Retrieves the latest cursor for a Dropbox folder.

```
GET https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/get-latest-folder-cursor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/get-latest-folder-cursor?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/get-latest-folder-cursor?${params}`, {
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
| `path` | string | no | The folder path or ID to get a latest cursor for. Leave blank to use the root folder. Example: `/Projects`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cursor` | string |  |

## Native endpoint

Through the native Dropbox API, this operation is `POST /files/list_folder/get_latest_cursor` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-latest-folder-cursor.md) for the provider-specific parameters and requirements.

