# ScrapFly: Extract With Template

Retrieves extracted data from ScrapFly using a template.

```
GET https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/extract-with-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapFly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/extract-with-template?connectionId=$CONNECTION_ID&body=%3Chtml%3E%3Cbody%3E%3Ch1%3EExample%3C%2Fh1%3E%3C%2Fbody%3E%3C%2Fhtml%3E&contentType=text%2Fhtml&extractionTemplate=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "body": "<html><body><h1>Example</h1></body></html>",
  "contentType": "text/html",
  "extractionTemplate": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/extract-with-template?${params}`, {
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
| `extractionTemplate` | string | yes | Stored or inline extraction template to apply to the provided document. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ScrapFly API returns.

## Native endpoint

Through the native ScrapFly API, this operation is `POST /extraction` (base URL `https://api.scrapfly.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-with-template.md) for the provider-specific parameters and requirements.

