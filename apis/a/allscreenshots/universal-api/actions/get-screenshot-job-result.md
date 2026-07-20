# Allscreenshots: Get Screenshot Job Result

Retrieves the completed result of an async screenshot job in Allscreenshots.

```
GET https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/get-screenshot-job-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Allscreenshots `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/get-screenshot-job-result?connectionId=$CONNECTION_ID&job_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "job_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/get-screenshot-job-result?${params}`, {
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
| `job_id` | string | yes | The async screenshot job whose result you want to download. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cached": true,
      "contentType": "string",
      "data": "string",
      "encoding": "string",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "format": "string",
      "height": 1,
      "renderTimeMs": 1,
      "size": 1,
      "storageUrl": "https://example.com",
      "url": "https://example.com",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cached` | boolean |  |
| `contentType` | string |  |
| `data` | string |  |
| `encoding` | string |  |
| `expiresAt` | date |  |
| `format` | string |  |
| `height` | number |  |
| `renderTimeMs` | number |  |
| `size` | number |  |
| `storageUrl` | string |  |
| `url` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Allscreenshots API, this operation is `GET /v1/screenshots/jobs/:jobId/result` (base URL `https://api.allscreenshots.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-screenshot-job-result.md) for the provider-specific parameters and requirements.

