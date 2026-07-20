# Print.one Postcards: Get Template Preview Details

Retrieves template preview details from Print.one Postcards.

```
GET https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/get-template-preview-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Print.one Postcards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/get-template-preview-details?connectionId=$CONNECTION_ID&previewId=string&asPdf=true" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "previewId": "string",
  "asPdf": "true"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/get-template-preview-details?${params}`, {
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
| `previewId` | string | yes | The ID of the preview |
| `asPdf` | boolean | yes | Whether the preview was rendered as a PDF |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ],
      "id": "string",
      "imageUrl": "https://example.com",
      "templateId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> |  |
| `id` | string |  |
| `imageUrl` | string |  |
| `templateId` | string |  |

## Native endpoint

Through the native Print.one Postcards API, this operation is `GET /v2/storage/template/preview/[:previewId]/details` (base URL `https://api.print.one`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template-preview-details.md) for the provider-specific parameters and requirements.

