# GitBook: List Change Requests

Retrieves change requests from a GitBook space.

```
GET https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/list-change-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitBook `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/list-change-requests?connectionId=$CONNECTION_ID&limit=25&offset=0&spaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "spaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/list-change-requests?${params}`, {
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
| `contributor` | string | no |  |
| `creator` | string | no |  |
| `orderBy` | string | no |  |
| `requestedReviewer` | string | no |  |
| `spaceId` | string | yes |  |
| `status` | string | no |  |
| `topic` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {
        "displayName": "Ava Chen",
        "email": "ava@example.com",
        "id": "string"
      },
      "id": "string",
      "number": 1,
      "object": "string",
      "outdated": true,
      "revision": "string",
      "revisionInitial": "string",
      "space": "string",
      "status": "string",
      "subject": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "urls": {
        "app": "https://example.com",
        "location": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | number |  |
| `createdAt` | date |  |
| `createdBy.displayName` | string |  |
| `createdBy.email` | string |  |
| `createdBy.id` | string |  |
| `id` | string |  |
| `number` | number |  |
| `object` | string |  |
| `outdated` | boolean |  |
| `revision` | string |  |
| `revisionInitial` | string |  |
| `space` | string |  |
| `status` | string |  |
| `subject` | string |  |
| `updatedAt` | date |  |
| `urls.app` | string |  |
| `urls.location` | string |  |

## Native endpoint

Through the native GitBook API, this operation is `GET /spaces/:spaceId/change-requests` (base URL `https://api.gitbook.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-change-requests.md) for the provider-specific parameters and requirements.

