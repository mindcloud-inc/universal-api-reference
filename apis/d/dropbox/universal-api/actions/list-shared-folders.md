# Dropbox: List Shared Folders

Retrieves shared folders for the current user from Dropbox.

```
GET https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/list-shared-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/list-shared-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/list-shared-folders?${params}`, {
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
| `limit` | number | no | Maximum number of shared folders to return. Example: `100`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `actions` | list<string> | no | Optional list of folder actions to filter for. Leave blank to return all shared folders. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entries": [
        {
          "accessInheritance": {
            "tag": "string"
          },
          "accessType": {
            "tag": "string"
          },
          "isInsideTeamFolder": true,
          "isTeamFolder": true,
          "name": "Ava Chen",
          "pathDisplay": "string",
          "pathLower": "string",
          "policy": {
            "aclUpdatePolicy": {
              "tag": "string"
            },
            "sharedLinkPolicy": {
              "tag": "https://example.com"
            },
            "viewerInfoPolicy": {
              "tag": "string"
            }
          },
          "previewUrl": "https://example.com",
          "sharedFolderId": "string",
          "timeInvited": "2026-05-07T12:00:00.000Z"
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
| `entries[].accessInheritance.tag` | string |  |
| `entries[].accessType.tag` | string |  |
| `entries[].isInsideTeamFolder` | boolean |  |
| `entries[].isTeamFolder` | boolean |  |
| `entries[].name` | string |  |
| `entries[].pathDisplay` | string |  |
| `entries[].pathLower` | string |  |
| `entries[].policy.aclUpdatePolicy.tag` | string |  |
| `entries[].policy.sharedLinkPolicy.tag` | string |  |
| `entries[].policy.viewerInfoPolicy.tag` | string |  |
| `entries[].previewUrl` | string |  |
| `entries[].sharedFolderId` | string |  |
| `entries[].timeInvited` | date |  |

## Native endpoint

Through the native Dropbox API, this operation is `POST /sharing/list_folders` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shared-folders.md) for the provider-specific parameters and requirements.

