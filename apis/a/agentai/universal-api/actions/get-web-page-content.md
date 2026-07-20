# Agent.ai: Get Web Page Content

Retrieves web page text from Agent.ai by URL or domain.

```
GET https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-web-page-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-web-page-content?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-web-page-content?${params}`, {
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
| `url` | string | yes | URL of the web page to extract text from. |
| `mode` | string | no | Crawler mode: scrape for one page, crawl for up to 100 pages. Default: `scrape`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": {},
      "response": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metadata` | object | Metadata extracted from the target web page. |
| `response` | string | Extracted text content from the requested web page or domain. |
| `status` | number | HTTP status code returned by Agent.ai for the action response. |

## Native endpoint

Through the native Agent.ai API, this operation is `POST /action/grab_web_text` (base URL `https://api-lr.agent.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-web-page-content.md) for the provider-specific parameters and requirements.

