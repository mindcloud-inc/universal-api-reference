# Dropbox: Search Files and Folders

Finds files and folders in Dropbox by search query.

```
GET https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/search-files-and-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/search-files-and-folders?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/search-files-and-folders?${params}`, {
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
| `query` | string | yes | The search string to look for across files and folders. |
| `options.path` | string | no | Optional folder path to scope the search. Example: `/MindCloud Dropbox Test`. |
| `options.maxResults` | number | no | Maximum number of matches to return, from 1 to 1000. Example: `10`. |
| `options.filenameOnly` | boolean | no | When enabled, only file and folder names are searched. |
| `matchFieldOptions.includeHighlights` | boolean | no | When enabled, include title highlight spans in the match fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasMore": true,
      "matches": [
        {
          "matchType": {
            "tag": "string"
          },
          "metadata": {
            "metadata": {
              "clientModified": "2026-05-07T12:00:00.000Z",
              "contentHash": "string",
              "fileOwnerTeamEncryptedId": "string",
              "id": "string",
              "isDownloadable": true,
              "name": "Ava Chen",
              "pathDisplay": "string",
              "pathLower": "string",
              "rev": "string",
              "serverModified": "2026-05-07T12:00:00.000Z",
              "size": 1,
              "tag": "string"
            },
            "tag": "string"
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasMore` | boolean |  |
| `matches[].matchType.tag` | string |  |
| `matches[].metadata.metadata.clientModified` | date |  |
| `matches[].metadata.metadata.contentHash` | string |  |
| `matches[].metadata.metadata.fileOwnerTeamEncryptedId` | string |  |
| `matches[].metadata.metadata.id` | string |  |
| `matches[].metadata.metadata.isDownloadable` | boolean |  |
| `matches[].metadata.metadata.name` | string |  |
| `matches[].metadata.metadata.pathDisplay` | string |  |
| `matches[].metadata.metadata.pathLower` | string |  |
| `matches[].metadata.metadata.rev` | string |  |
| `matches[].metadata.metadata.serverModified` | date |  |
| `matches[].metadata.metadata.size` | number |  |
| `matches[].metadata.metadata.tag` | string |  |
| `matches[].metadata.tag` | string |  |

## Native endpoint

Through the native Dropbox API, this operation is `POST /files/search_v2` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-files-and-folders.md) for the provider-specific parameters and requirements.

