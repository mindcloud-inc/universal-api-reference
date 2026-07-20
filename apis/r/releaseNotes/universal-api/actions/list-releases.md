# ReleaseNotes: List Releases

Retrieves releases from ReleaseNotes.

```
GET https://connect.mindcloud.co/v1/universal/releaseNotes/latest/actions/list-releases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReleaseNotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/releaseNotes/latest/actions/list-releases?connectionId=$CONNECTION_ID&projectId=11233" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "11233"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/releaseNotes/latest/actions/list-releases?${params}`, {
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
| `projectId` | string | yes | The numeric Project ID shown in ReleaseNotes URLs like /manage/project/1234/releases/4321. Example: `11233`. |
| `page` | string | no | Optional page number for paginated release results. Example: `1`. |
| `tags` | string | no | Optional comma-separated tag names to filter releases, for example article,editor. Example: `article,editor`. |
| `releasedSince` | string | no | Optional YYYY-MM-DD date to return only releases published on or after that date. Example: `2022-10-01`. |

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
      "involved": [
        {
          "avatar": "string",
          "name": "Ava Chen"
        }
      ],
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
| `involved[].avatar` | string |  |
| `involved[].name` | string |  |
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

Through the native ReleaseNotes API, this operation is `GET /projects/:projectId/releases` (base URL `https://api.releasenotes.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-releases.md) for the provider-specific parameters and requirements.

