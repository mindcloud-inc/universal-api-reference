# GitBook: Create Change Request

Creates a new change request in GitBook.

```
POST https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/create-change-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/create-change-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/create-change-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spaceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `spaceId` | string | yes |  |
| `subject` | string | no |  |

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

Through the native GitBook API, this operation is `POST /spaces/:spaceId/change-requests` (base URL `https://api.gitbook.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-change-request.md) for the provider-specific parameters and requirements.

