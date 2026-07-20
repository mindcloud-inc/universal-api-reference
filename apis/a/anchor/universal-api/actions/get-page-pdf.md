# Anchor: Get Page PDF

Retrieves a webpage PDF from Anchor.

```
GET https://connect.mindcloud.co/v1/universal/anchor/latest/actions/get-page-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anchor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anchor/latest/actions/get-page-pdf?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anchor/latest/actions/get-page-pdf?${params}`, {
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
| `url` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pdf": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pdf` | string |  |

## Native endpoint

Through the native Anchor API, this operation is `POST /v1/tools/page-pdf` (base URL `https://api.anchorbrowser.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page-pdf.md) for the provider-specific parameters and requirements.

