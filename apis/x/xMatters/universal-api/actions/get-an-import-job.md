# xMatters: Get an import job

Retrieves an import job from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-an-import-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-an-import-job?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-an-import-job?${params}`, {
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
| `importId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "by": {
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "links": {
          "self": "https://example.com"
        },
        "recipientType": "string",
        "targetName": "Ava Chen"
      },
      "finishedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "name": "Ava Chen",
      "processedCount": 1,
      "processingAt": "2026-05-07T12:00:00.000Z",
      "started": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "totalCount": 1,
      "transform": {
        "name": "Ava Chen",
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `by.firstName` | string |  |
| `by.id` | string |  |
| `by.lastName` | string |  |
| `by.links.self` | string |  |
| `by.recipientType` | string |  |
| `by.targetName` | string |  |
| `finishedAt` | date |  |
| `id` | string |  |
| `links.self` | string |  |
| `name` | string |  |
| `processedCount` | number |  |
| `processingAt` | date |  |
| `started` | date |  |
| `status` | string |  |
| `totalCount` | number |  |
| `transform.name` | string |  |
| `transform.url` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `GET imports/{importId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-an-import-job.md) for the provider-specific parameters and requirements.

