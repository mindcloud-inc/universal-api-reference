# Zoho Backstage: List Events



```
GET https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Backstage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-events?connectionId=$CONNECTION_ID&portalId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-events?${params}`, {
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
| `portalId` | string | yes | The Zoho Backstage portal ID. |
| `status` | string | no | Filter events by lifecycle status. |
| `sortBy` | string | no | Sort events by a supported field. |
| `sortOrder` | string | no | Sort direction for the event list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "createdBy": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string"
      },
      "createdTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "endTime": "2026-05-07T12:00:00.000Z",
      "eventType": 1,
      "eventTypeString": "string",
      "id": "string",
      "language": "string",
      "lastModifiedBy": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string"
      },
      "lastModifiedTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "socialHandles": {
        "website": "string"
      },
      "space": {
        "id": "string"
      },
      "startTime": "2026-05-07T12:00:00.000Z",
      "status": 1,
      "statusString": "string",
      "summary": "string",
      "tags": [
        "string"
      ],
      "thumbnailUrl": "https://example.com",
      "timezone": "string",
      "websiteUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `createdBy.email` | string |  |
| `createdBy.firstName` | string |  |
| `createdBy.id` | string |  |
| `createdTime` | date |  |
| `description` | string |  |
| `endTime` | date |  |
| `eventType` | number |  |
| `eventTypeString` | string |  |
| `id` | string |  |
| `language` | string |  |
| `lastModifiedBy.email` | string |  |
| `lastModifiedBy.firstName` | string |  |
| `lastModifiedBy.id` | string |  |
| `lastModifiedTime` | date |  |
| `name` | string |  |
| `socialHandles.website` | string |  |
| `space.id` | string |  |
| `startTime` | date |  |
| `status` | number |  |
| `statusString` | string |  |
| `summary` | string |  |
| `tags` | array<string> |  |
| `thumbnailUrl` | string |  |
| `timezone` | string |  |
| `websiteUrl` | string |  |

## Native endpoint

Through the native Zoho Backstage API, this operation is `GET /v3/portals/:portal_id/events` (base URL `https://zohoapis.com/backstage`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

