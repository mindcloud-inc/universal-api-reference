# ReleaseNotes: Create or Update Release

Creates or updates a release in ReleaseNotes.

```
POST https://connect.mindcloud.co/v1/universal/releaseNotes/latest/actions/create-or-update-release
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReleaseNotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/releaseNotes/latest/actions/create-or-update-release" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "11233",
  "title": "March 2026 Dashboard Improvements"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/releaseNotes/latest/actions/create-or-update-release', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "11233",
    "title": "March 2026 Dashboard Improvements"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The numeric Project ID shown in ReleaseNotes URLs like /manage/project/1234/releases/4321. Example: `11233`. |
| `title` | string | yes | The release title shown to end users. Example: `March 2026 Dashboard Improvements`. |
| `description` | string | no | The main body content for the release. Example: `We shipped a small set of dashboard improvements to make daily work faster.`. |
| `externalId` | string | no | Optional external identifier. If it matches an existing release, ReleaseNotes updates that release instead of creating a new one. Example: `dashboard-release-2026-03`. |
| `featuredImage` | string | no | Optional featured image URL for the release. Example: `https://example.com/images/dashboard-release.png`. |
| `type` | string | no | Optional release type. The docs list update, bugfix, and feature. Default: `update`. Example: `update`. |
| `owner` | string | no | Optional owner email address for the release. Example: `release.owner@example.com`. |
| `status` | string | no | Optional publication status. The docs list published and pending. Default: `published`. Example: `published`. |
| `private` | boolean | no | Optional boolean that controls whether the release is private. Default: `false`. |
| `releasedAt` | string | no | Optional release timestamp using the provider format YYYY-MM-DD h:m:i. Example: `2026-03-26 10:30:00`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "externalId": "string",
      "featuredImage": "string",
      "featuredImageUrl": "https://example.com",
      "id": "string",
      "owner": {
        "avatar": "string",
        "name": "Ava Chen"
      },
      "private": true,
      "releasedAt": 1,
      "releasedAtHuman": "string",
      "socialImage": "string",
      "status": "string",
      "title": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `externalId` | string |  |
| `featuredImage` | string |  |
| `featuredImageUrl` | string |  |
| `id` | string |  |
| `owner.avatar` | string |  |
| `owner.name` | string |  |
| `private` | boolean |  |
| `releasedAt` | number |  |
| `releasedAtHuman` | string |  |
| `socialImage` | string |  |
| `status` | string |  |
| `title` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native ReleaseNotes API, this operation is `POST /projects/:projectId/releases` (base URL `https://api.releasenotes.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-release.md) for the provider-specific parameters and requirements.

