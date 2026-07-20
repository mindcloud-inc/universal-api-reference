# Casting42: Search Talent Photos

Finds talent photos in Casting42 by talent tag.

```
GET https://connect.mindcloud.co/v1/universal/casting42/latest/actions/search-talent-photos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Casting42 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/casting42/latest/actions/search-talent-photos?connectionId=$CONNECTION_ID&talentTags%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "talentTags[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/casting42/latest/actions/search-talent-photos?${params}`, {
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
| `talentTags[]` | array<string> | yes | Array of talent tags to search photos for. |
| `photoSize` | string | no | Requested photo size, such as large. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachmentLabel": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "filename": "Ava Chen",
      "isProfilePicture": true,
      "tag": "string",
      "talentTag": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachmentLabel` | string | Attachment label. |
| `createdAt` | date | Photo creation timestamp. |
| `filename` | string | Photo filename. |
| `isProfilePicture` | boolean | Whether the photo is marked as the profile picture. |
| `tag` | string | Photo tag. |
| `talentTag` | string | Related talent tag. |
| `url` | string | Photo download URL. |

## Native endpoint

Through the native Casting42 API, this operation is `POST /api/v2/talents/photos/find` (base URL `https://casting42.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-talent-photos.md) for the provider-specific parameters and requirements.

