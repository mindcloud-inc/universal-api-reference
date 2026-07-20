# LLMWhisperer: Start Extraction From URL

Starts a document extraction job in LLMWhisperer from a URL.

```
POST https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/start-extraction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LLMWhisperer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/start-extraction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/start-extraction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Publicly accessible URL of the document to extract. This action uses the documented URL submission path for /whisper. |
| `mode` | string | no | Processing mode such as native_text, low_cost, high_quality, form, or table. Default: `form`. |
| `outputMode` | string | no | Choose layout_preserving or text output. Default: `layout_preserving`. |
| `pagesToExtract` | string | no | Comma/range page selector such as 1-5,7,21-. |
| `tag` | string | no | Audit tag used in usage reports. Default: `default`. |
| `fileName` | string | no | Audit file name value stored with the extraction run. |
| `useWebhook` | string | no | Previously registered webhook name to notify after processing completes. |
| `addLineNos` | boolean | no | Include line numbers and save highlight metadata. Default: `false`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageSeparator` | string | no | String inserted between extracted pages. Default: `<<<`. |
| `lineSplitterTolerance` | number | no | Baseline tolerance factor for line splitting. Default: `0.4`. |
| `horizontalStretchFactor` | number | no | Horizontal stretch factor for difficult layouts. Default: `1.0`. |
| `lineSplitterStrategy` | string | no | Advanced line splitter strategy. Default: `left-priority`. |
| `medianFilterSize` | number | no | Median filter size for low_cost mode noise reduction. Default: `0`. |
| `gaussianBlurRadius` | number | no | Gaussian blur radius for low_cost mode noise reduction. Default: `0`. |
| `markVerticalLines` | boolean | no | Preserve vertical lines when supported. Default: `false`. |
| `markHorizontalLines` | boolean | no | Preserve horizontal lines when supported. Default: `false`. |
| `lang` | string | no | OCR language hint. Default: `eng`. |
| `webhookMetadata` | string | no | Metadata string sent verbatim to the webhook callback. |
| `allowRotatedText` | boolean | no | Preserve rotated or angled text when supported. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string",
      "whisper_hash": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | string |  |
| `whisper_hash` | string |  |

## Native endpoint

Through the native LLMWhisperer API, this operation is `POST /whisper` (base URL `https://llmwhisperer-api.us-central.unstract.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-extraction.md) for the provider-specific parameters and requirements.

