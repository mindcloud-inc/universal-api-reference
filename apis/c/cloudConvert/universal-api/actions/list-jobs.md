# CloudConvert: List Jobs

Retrieves jobs from your CloudConvert account.

```
GET https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/list-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudConvert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/list-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/list-jobs?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "endedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "startedAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "tag": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `endedAt` | date |  |
| `id` | string |  |
| `links.self` | string |  |
| `startedAt` | date |  |
| `status` | string |  |
| `tag` | string |  |

## Native endpoint

Through the native CloudConvert API, this operation is `GET /jobs` (base URL `https://api.cloudconvert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-jobs.md) for the provider-specific parameters and requirements.

