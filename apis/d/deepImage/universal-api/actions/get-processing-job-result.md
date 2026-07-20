# DeepImage: Get Processing Job Result

Retrieves a completed processing job result from DeepImage.

```
GET https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/get-processing-job-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeepImage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/get-processing-job-result?connectionId=$CONNECTION_ID&hash=a8784c00-dc6b-11ee-ad50-9ec3ba0205c0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hash": "a8784c00-dc6b-11ee-ad50-9ec3ba0205c0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/get-processing-job-result?${params}`, {
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
| `hash` | string | yes | The processing job hash returned by Queue Image Processing Job or a wrapper action. Example: `a8784c00-dc6b-11ee-ad50-9ec3ba0205c0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job": "string",
      "queue": 1,
      "result_url": "https://example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job` | string | DeepImage processing job identifier. |
| `queue` | number | Queue position when DeepImage reports it. |
| `result_url` | string | URL of the processed image when available. |
| `status` | string | Processing status returned by DeepImage. |

## Native endpoint

Through the native DeepImage API, this operation is `GET /rest_api/result/:hash` (base URL `https://deep-image.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-processing-job-result.md) for the provider-specific parameters and requirements.

