# Dropbox: List Folder Contents

Retrieves the contents of a Dropbox folder.

```
GET https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/list-folder-contents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/list-folder-contents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/list-folder-contents?${params}`, {
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
| `path` | string | no | The folder path or ID to list. Leave blank to list the root folder. Example: `/Projects`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string",
      "entries": [
        {
          "id": "string",
          "name": "Ava Chen",
          "pathDisplay": "string",
          "pathLower": "string",
          "tag": "string"
        }
      ],
      "hasMore": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cursor` | string |  |
| `entries[].id` | string |  |
| `entries[].name` | string |  |
| `entries[].pathDisplay` | string |  |
| `entries[].pathLower` | string |  |
| `entries[].tag` | string |  |
| `hasMore` | boolean |  |

## Native endpoint

Through the native Dropbox API, this operation is `POST /files/list_folder` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-folder-contents.md) for the provider-specific parameters and requirements.

