# ReleaseNotes: Search Subscribers

Finds subscribers in ReleaseNotes by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/releaseNotes/latest/actions/search-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReleaseNotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/releaseNotes/latest/actions/search-subscribers?connectionId=$CONNECTION_ID&projectId=11233&q=nobody%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "11233",
  "q": "nobody@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/releaseNotes/latest/actions/search-subscribers?${params}`, {
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
| `q` | string | yes | The email address or partial subscriber value to search for. Example: `nobody@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedVia": "string",
      "createdAt": "string",
      "id": 1,
      "medium": "string",
      "name": "Ava Chen",
      "teamId": 1,
      "uid": "string",
      "unsubscribedAt": "string",
      "updatedAt": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedVia` | string |  |
| `createdAt` | string |  |
| `id` | number |  |
| `medium` | string |  |
| `name` | string |  |
| `teamId` | number |  |
| `uid` | string |  |
| `unsubscribedAt` | string |  |
| `updatedAt` | string |  |
| `value` | string |  |

## Native endpoint

Through the native ReleaseNotes API, this operation is `POST /projects/:projectId/subscribers/search` (base URL `https://api.releasenotes.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-subscribers.md) for the provider-specific parameters and requirements.

