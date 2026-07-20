# Olostep: Retrieve Content

Retrieves content by retrieve ID from Olostep.

```
GET https://connect.mindcloud.co/v1/universal/olostep/latest/actions/retrieve-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Olostep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/olostep/latest/actions/retrieve-content?connectionId=$CONNECTION_ID&retrieveId=ret_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "retrieveId": "ret_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/olostep/latest/actions/retrieve-content?${params}`, {
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
| `retrieveId` | string | yes | Retrieve ID from a crawl page, scrape, or batch item response. Example: `ret_123`. |
| `formats[]` | array<string> | no | Optional formats to return. Choose one or more of html, markdown, or json. If omitted, all available formats are returned. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "htmlContent": {},
      "htmlHostedUrl": {},
      "jsonContent": {},
      "jsonHostedUrl": {},
      "markdownContent": "string",
      "markdownHostedUrl": "https://example.com",
      "networkCalls": {},
      "screenshotHostedUrl": {},
      "sizeExceeded": true,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `htmlContent` | object |  |
| `htmlHostedUrl` | object |  |
| `jsonContent` | object |  |
| `jsonHostedUrl` | object |  |
| `markdownContent` | string |  |
| `markdownHostedUrl` | string |  |
| `networkCalls` | object |  |
| `screenshotHostedUrl` | object |  |
| `sizeExceeded` | boolean |  |
| `success` | boolean |  |

## Native endpoint

Through the native Olostep API, this operation is `GET /v1/retrieve` (base URL `https://api.olostep.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-content.md) for the provider-specific parameters and requirements.

