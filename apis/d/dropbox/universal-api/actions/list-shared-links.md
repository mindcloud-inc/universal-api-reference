# Dropbox: List Shared Links

Retrieves shared links for the current user from Dropbox.

```
GET https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/list-shared-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/list-shared-links?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/list-shared-links?${params}`, {
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
| `path` | string | no | Path to a file or folder. When omitted, Dropbox returns the current user's shared links. |
| `directOnly` | boolean | no | When true, return only links directly on the path instead of inherited links. Example: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cursor` | string | no | Cursor returned by a previous List Shared Links call. Example: `AAFdGEp0n3QAAAAAAAABaQ`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasMore": true,
      "links": [
        {
          "clientModified": "2026-05-07T12:00:00.000Z",
          "id": "https://example.com",
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
          "name": "https://example.com",
          "pathLower": "https://example.com",
          "previewType": "https://example.com",
          "rev": "https://example.com",
          "serverModified": "2026-05-07T12:00:00.000Z",
          "size": 1,
          "tag": "https://example.com",
          "url": "https://example.com"
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
| `links[].clientModified` | date |  |
| `links[].id` | string |  |
| `links[].linkPermissions.allowComments` | boolean |  |
| `links[].linkPermissions.allowDownload` | boolean |  |
| `links[].linkPermissions.audienceOptions[].allowed` | boolean |  |
| `links[].linkPermissions.audienceOptions[].audience.tag` | string |  |
| `links[].linkPermissions.canAllowDownload` | boolean |  |
| `links[].linkPermissions.canDisallowDownload` | boolean |  |
| `links[].linkPermissions.canRemoveExpiry` | boolean |  |
| `links[].linkPermissions.canRemovePassword` | boolean |  |
| `links[].linkPermissions.canRequestAccess` | boolean |  |
| `links[].linkPermissions.canRevoke` | boolean |  |
| `links[].linkPermissions.canSetExpiry` | boolean |  |
| `links[].linkPermissions.canSetPassword` | boolean |  |
| `links[].linkPermissions.canSync` | boolean |  |
| `links[].linkPermissions.canUseExtendedSharingControls` | boolean |  |
| `links[].linkPermissions.effectiveAudience.tag` | string |  |
| `links[].linkPermissions.linkAccessLevel.tag` | string |  |
| `links[].linkPermissions.requestedVisibility.tag` | string |  |
| `links[].linkPermissions.requirePassword` | boolean |  |
| `links[].linkPermissions.resolvedVisibility.tag` | string |  |
| `links[].linkPermissions.teamRestrictsComments` | boolean |  |
| `links[].linkPermissions.visibilityPolicies[].allowed` | boolean |  |
| `links[].linkPermissions.visibilityPolicies[].policy.tag` | string |  |
| `links[].linkPermissions.visibilityPolicies[].resolvedPolicy.tag` | string |  |
| `links[].name` | string |  |
| `links[].pathLower` | string |  |
| `links[].previewType` | string |  |
| `links[].rev` | string |  |
| `links[].serverModified` | date |  |
| `links[].size` | number |  |
| `links[].tag` | string |  |
| `links[].url` | string |  |

## Native endpoint

Through the native Dropbox API, this operation is `POST /sharing/list_shared_links` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shared-links.md) for the provider-specific parameters and requirements.

