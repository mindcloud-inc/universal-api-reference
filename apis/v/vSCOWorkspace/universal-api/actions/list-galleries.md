# VSCO Workspace: List Galleries

Retrieves galleries from VSCO Workspace.

```
GET https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/list-galleries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VSCO Workspace `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/list-galleries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/list-galleries?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "adminUrl": "https://example.com",
      "category": "string",
      "clientUrl": "https://example.com",
      "coverPhoto": {},
      "created": "2026-05-07T12:00:00.000Z",
      "eventDate": "2026-05-07T12:00:00.000Z",
      "eventId": "string",
      "expirationDate": "2026-05-07T12:00:00.000Z",
      "externalMappings": [
        {}
      ],
      "headline": "string",
      "hidden": true,
      "id": "string",
      "jobId": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "orderCount": 1,
      "orderDueDate": "2026-05-07T12:00:00.000Z",
      "password": "string",
      "photoCount": 1,
      "public": true,
      "releaseDate": "2026-05-07T12:00:00.000Z",
      "remoteCreated": {},
      "remoteId": "string",
      "requiresPassword": true,
      "slug": "string",
      "status": "string",
      "visitorCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminUrl` | string | The internal URL of this gallery in the remote admin portal. May be used to link employees to the gallery administration interface in the remote service. |
| `category` | string | The category of this gallery. Galleries may be grouped by this category text in future client portal designs. |
| `clientUrl` | string | The URL of this gallery. Will be used for links in emails and the client portal. |
| `coverPhoto` | object | When creating or updating a gallery, this object may be used to import a cover photo. If the gallery does not yet have a covor photo, VSCO Workspace will use a placeholder graphic. |
| `created` | date | A server timestamp (always in UTC) |
| `eventDate` | date | The date of the event this gallery is for. Useful in automations or email tokens. |
| `eventId` | string | A ULID entity identifier that is nullable. |
| `expirationDate` | date | The date this gallery will expire and no longer be accessible. Useful in automations or email tokens. |
| `externalMappings` | array<object> |  |
| `headline` | string | The headline of this gallery. Prioritized over name when displayed to the user. |
| `hidden` | boolean | Whether or not the object is hidden. |
| `id` | string | A lowercase [ULID](https://github.com/ulid/spec) entity identifier |
| `jobId` | string | A ULID entity identifier that is nullable. |
| `modified` | date | A server timestamp (always in UTC) |
| `name` | string | The name of this gallery. |
| `orderCount` | number | The number of orders placed for this gallery. |
| `orderDueDate` | date | The date that orders for this gallery are due by. Useful in automations or email tokens. |
| `password` | string | A reusable plain-text passcode for unlocking the gallery. This pass code may be given to invited users. |
| `photoCount` | number | The number of photos in this gallery. |
| `public` | boolean | Whether this gallery is publicly accessible. |
| `releaseDate` | date | The date this gallery will be released to the public. Useful in automations or email tokens. |
| `remoteCreated` | object |  |
| `remoteId` | string | The remote ID of this gallery. <b>This value must be unique for the studio.</b> |
| `requiresPassword` | boolean |  |
| `slug` | string | The URL path slug for this gallery. This is the URL-friendly version of the name and must contain only letters, numbers, dashes, and underscores. When setting this value, it will be converted to lowercase and any illegal characters stripped. |
| `status` | string |  |
| `visitorCount` | number | The number of visitors to this gallery. |

## Native endpoint

Through the native VSCO Workspace API, this operation is `GET /gallery` (base URL `https://workspace.vsco.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-galleries.md) for the provider-specific parameters and requirements.

