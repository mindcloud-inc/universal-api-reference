# Dropbox: Get Shared Link Metadata

Retrieves metadata for a Dropbox shared link.

```
GET https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/get-shared-link-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/get-shared-link-metadata?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fwww.dropbox.com%2Fscl%2Ffi%2Fexample%2Ffile.txt%3Frlkey%3Dabc123%26dl%3D0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://www.dropbox.com/scl/fi/example/file.txt?rlkey=abc123&dl=0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/get-shared-link-metadata?${params}`, {
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
| `url` | string | yes | Shared link URL to inspect. Example: `https://www.dropbox.com/scl/fi/example/file.txt?rlkey=abc123&dl=0`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `path` | string | no | Optional relative path inside the shared link. Example: `/nested/file.txt`. |
| `linkPassword` | string | no | Password for a password-protected shared link. Example: `secret123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientModified": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "linkPermissions": {
        "allowComments": true,
        "allowDownload": true,
        "audienceOptions": [
          {
            "allowed": true,
            "audience": {
              "tag": "https://example.com"
            }
          }
        ],
        "canAllowDownload": true,
        "canDisallowDownload": true,
        "canRemoveExpiry": true,
        "canRemovePassword": true,
        "canRequestAccess": true,
        "canRevoke": true,
        "canSetExpiry": true,
        "canSetPassword": true,
        "canSync": true,
        "canUseExtendedSharingControls": true,
        "effectiveAudience": {
          "tag": "https://example.com"
        },
        "linkAccessLevel": {
          "tag": "https://example.com"
        },
        "requestedVisibility": {
          "tag": "https://example.com"
        },
        "requirePassword": true,
        "resolvedVisibility": {
          "tag": "https://example.com"
        },
        "teamRestrictsComments": true,
        "visibilityPolicies": [
          {
            "allowed": true,
            "policy": {
              "tag": "https://example.com"
            },
            "resolvedPolicy": {
              "tag": "https://example.com"
            }
          }
        ]
      },
      "name": "Ava Chen",
      "pathLower": "string",
      "previewType": "string",
      "rev": "string",
      "serverModified": "2026-05-07T12:00:00.000Z",
      "size": 1,
      "tag": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientModified` | date |  |
| `id` | string |  |
| `linkPermissions.allowComments` | boolean |  |
| `linkPermissions.allowDownload` | boolean |  |
| `linkPermissions.audienceOptions[].allowed` | boolean |  |
| `linkPermissions.audienceOptions[].audience.tag` | string |  |
| `linkPermissions.canAllowDownload` | boolean |  |
| `linkPermissions.canDisallowDownload` | boolean |  |
| `linkPermissions.canRemoveExpiry` | boolean |  |
| `linkPermissions.canRemovePassword` | boolean |  |
| `linkPermissions.canRequestAccess` | boolean |  |
| `linkPermissions.canRevoke` | boolean |  |
| `linkPermissions.canSetExpiry` | boolean |  |
| `linkPermissions.canSetPassword` | boolean |  |
| `linkPermissions.canSync` | boolean |  |
| `linkPermissions.canUseExtendedSharingControls` | boolean |  |
| `linkPermissions.effectiveAudience.tag` | string |  |
| `linkPermissions.linkAccessLevel.tag` | string |  |
| `linkPermissions.requestedVisibility.tag` | string |  |
| `linkPermissions.requirePassword` | boolean |  |
| `linkPermissions.resolvedVisibility.tag` | string |  |
| `linkPermissions.teamRestrictsComments` | boolean |  |
| `linkPermissions.visibilityPolicies[].allowed` | boolean |  |
| `linkPermissions.visibilityPolicies[].policy.tag` | string |  |
| `linkPermissions.visibilityPolicies[].resolvedPolicy.tag` | string |  |
| `name` | string |  |
| `pathLower` | string |  |
| `previewType` | string |  |
| `rev` | string |  |
| `serverModified` | date |  |
| `size` | number |  |
| `tag` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Dropbox API, this operation is `POST /sharing/get_shared_link_metadata` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shared-link-metadata.md) for the provider-specific parameters and requirements.

