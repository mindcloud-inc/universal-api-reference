# Dropbox: Create Shared Link

Creates a shared link in Dropbox, or returns an existing link.

```
POST https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/create-shared-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/create-shared-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "path": "/MindCloud Dropbox Test/dropbox-stage3-20260306-171004/restore-target.txt"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/create-shared-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "path": "/MindCloud Dropbox Test/dropbox-stage3-20260306-171004/restore-target.txt"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `path` | string | yes | Example: `/MindCloud Dropbox Test/dropbox-stage3-20260306-171004/restore-target.txt`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `settings.allowDownload` | boolean | no | Whether the new shared link should allow downloads. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientModified": "2026-05-07T12:00:00.000Z",
      "createdTimestamp": "2026-05-07T12:00:00.000Z",
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
        "canRevoke": true,
        "canSetExpiry": true,
        "canSetPassword": true,
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
| `createdTimestamp` | date |  |
| `id` | string |  |
| `linkPermissions.allowComments` | boolean |  |
| `linkPermissions.allowDownload` | boolean |  |
| `linkPermissions.audienceOptions[].allowed` | boolean |  |
| `linkPermissions.audienceOptions[].audience.tag` | string |  |
| `linkPermissions.canAllowDownload` | boolean |  |
| `linkPermissions.canDisallowDownload` | boolean |  |
| `linkPermissions.canRemoveExpiry` | boolean |  |
| `linkPermissions.canRemovePassword` | boolean |  |
| `linkPermissions.canRevoke` | boolean |  |
| `linkPermissions.canSetExpiry` | boolean |  |
| `linkPermissions.canSetPassword` | boolean |  |
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

Through the native Dropbox API, this operation is `POST /sharing/create_shared_link_with_settings` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shared-link.md) for the provider-specific parameters and requirements.

