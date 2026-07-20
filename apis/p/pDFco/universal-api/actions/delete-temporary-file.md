# PDF.co: Delete Temporary File

Deletes a temporary file from PDF.co.

```
DELETE https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/delete-temporary-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/delete-temporary-file?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFco/latest/actions/delete-temporary-file?${params}`, {
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
| `url` | string | yes | The temporary PDF.co file URL to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits": 1,
      "duration": 1,
      "error": true,
      "remainingCredits": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits` | number | Credits consumed by this request. |
| `duration` | number | Processing duration in ms. |
| `error` | boolean | Whether delete request failed. |
| `remainingCredits` | number | Remaining account credits. |
| `status` | number | Status code from PDF.co. |

## Native endpoint

Through the native PDF.co API, this operation is `POST /file/delete` (base URL `https://api.pdf.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-temporary-file.md) for the provider-specific parameters and requirements.

