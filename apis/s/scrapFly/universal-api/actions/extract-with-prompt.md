# ScrapFly: Extract With Prompt

Retrieves extracted data from ScrapFly using an LLM prompt.

```
GET https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/extract-with-prompt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapFly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/extract-with-prompt?connectionId=$CONNECTION_ID&body=%3Chtml%3E%3Cbody%3E%3Ch1%3EExample%3C%2Fh1%3E%3C%2Fbody%3E%3C%2Fhtml%3E&contentType=text%2Fhtml&extractionPrompt=Extract%20the%20page%20title%20and%20return%20JSON." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "body": "<html><body><h1>Example</h1></body></html>",
  "contentType": "text/html",
  "extractionPrompt": "Extract the page title and return JSON."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/extract-with-prompt?${params}`, {
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
| `body` | string | yes | Raw document content to extract from. Example: `<html><body><h1>Example</h1></body></html>`. |
| `contentType` | string | yes | Content type of the raw body, such as text/html or application/json. Example: `text/html`. |
| `extractionPrompt` | string | yes | LLM instruction describing what to extract from the provided document. Example: `Extract the page title and return JSON.`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ScrapFly API returns.

## Native endpoint

Through the native ScrapFly API, this operation is `POST /extraction` (base URL `https://api.scrapfly.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-with-prompt.md) for the provider-specific parameters and requirements.

