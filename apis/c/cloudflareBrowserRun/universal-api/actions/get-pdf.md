# Cloudflare Browser Run: Get PDF

Generates a webpage PDF in Cloudflare Browser Run.

```
GET https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/get-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudflare Browser Run `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/get-pdf?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/get-pdf?${params}`, {
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
| `html` | string | no | HTML content to render. Either HTML or URL must be set. |
| `url` | string | no | URL to navigate to. Either URL or HTML must be set. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pdfOptions` | object | no | Puppeteer PDF options such as format, margins, landscape, scale, and printBackground. |
| `cacheTTL` | number | no | Cache TTL in seconds. Set 0 to disable cache. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string |  |
| `result` | string |  |

## Native endpoint

Through the native Cloudflare Browser Run API, this operation is `POST /accounts/:accountId/browser-rendering/pdf` (base URL `https://api.cloudflare.com/client/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pdf.md) for the provider-specific parameters and requirements.

