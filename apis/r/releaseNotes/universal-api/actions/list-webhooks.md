# ReleaseNotes: List Webhooks

Retrieves webhooks from ReleaseNotes.

```
GET https://connect.mindcloud.co/v1/universal/releaseNotes/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReleaseNotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/releaseNotes/latest/actions/list-webhooks?connectionId=$CONNECTION_ID&projectId=11233" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "11233"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/releaseNotes/latest/actions/list-webhooks?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "event": "string",
      "fullUrl": "https://example.com",
      "id": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `event` | string |  |
| `fullUrl` | string |  |
| `id` | number |  |
| `url` | string |  |

## Native endpoint

Through the native ReleaseNotes API, this operation is `GET /projects/:projectId/webhooks` (base URL `https://api.releasenotes.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

