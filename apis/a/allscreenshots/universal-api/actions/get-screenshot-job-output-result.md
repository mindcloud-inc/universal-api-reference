# Allscreenshots: Get Screenshot Job Output Result

Retrieves a specific output from an async screenshot job in Allscreenshots.

```
GET https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/get-screenshot-job-output-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Allscreenshots `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/get-screenshot-job-output-result?connectionId=$CONNECTION_ID&job_id=string&output_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "job_id": "string",
  "output_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/get-screenshot-job-output-result?${params}`, {
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
| `job_id` | string | yes | The async screenshot job whose specific output you want to download. |
| `output_id` | string | yes | The output identifier from a multi-output job result. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "data": "string",
      "encoding": "string",
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string |  |
| `data` | string |  |
| `encoding` | string |  |
| `size` | number |  |

## Native endpoint

Through the native Allscreenshots API, this operation is `GET /v1/screenshots/jobs/:jobId/result/:outputId` (base URL `https://api.allscreenshots.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-screenshot-job-output-result.md) for the provider-specific parameters and requirements.

