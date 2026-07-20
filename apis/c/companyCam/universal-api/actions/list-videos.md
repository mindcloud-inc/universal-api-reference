# CompanyCam: List Videos

Returns videos visible to the authenticated user, sorted by
capture date (most recent first).

```
GET https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/list-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CompanyCam `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/list-videos?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/list-videos?${params}`, {
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
| `startDate` | date | no | Timestamp to return videos captured on or after the provided value. |
| `endDate` | date | no | timestamp to return videos captured on or before the provided value |
| `projectId` | string | no | Filter results to include videos captured at one of these Project IDs Accepts multiple values as an array. |
| `userIds` | list<number> | no | Filter results to include videos captured by one of these user IDs. Accepts multiple values as an array. |
| `groupIds` | list<number> | no | Filter results to include videos captured by one of these group IDs Accepts multiple values as an array. |
| `tagIds` | list<number> | no | Filter results to include videos tagged with one of these tag IDs Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capturedAt": "2026-05-07T12:00:00.000Z",
      "companyId": "string",
      "coordinates": {
        "lat": 1,
        "lon": 1
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "creatorName": "Ava Chen",
      "creatorType": "string",
      "duration": 1,
      "format": "string",
      "id": "string",
      "internal": true,
      "playbackUrl": "https://example.com",
      "projectId": "string",
      "status": "string",
      "thumbnailUrls": {
        "large": "https://example.com",
        "medium": "https://example.com",
        "small": "https://example.com"
      },
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capturedAt` | date |  |
| `companyId` | string |  |
| `coordinates.lat` | number |  |
| `coordinates.lon` | number |  |
| `createdAt` | date |  |
| `creatorId` | string |  |
| `creatorName` | string |  |
| `creatorType` | string |  |
| `duration` | number |  |
| `format` | string |  |
| `id` | string |  |
| `internal` | boolean |  |
| `playbackUrl` | string |  |
| `projectId` | string |  |
| `status` | string |  |
| `thumbnailUrls.large` | string |  |
| `thumbnailUrls.medium` | string |  |
| `thumbnailUrls.small` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native CompanyCam API, this operation is `GET videos` (base URL `https://api.companycam.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-videos.md) for the provider-specific parameters and requirements.

