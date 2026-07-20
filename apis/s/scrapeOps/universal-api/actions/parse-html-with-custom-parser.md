# ScrapeOps: Parse Html With Custom Parser

Parses HTML with a ScrapeOps custom parser.

```
GET https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/parse-html-with-custom-parser
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeOps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/parse-html-with-custom-parser?connectionId=$CONNECTION_ID&customParserId=string&html=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customParserId": "string",
  "html": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/parse-html-with-custom-parser?${params}`, {
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
| `customParserId` | string | yes | The ScrapeOps custom parser ID created in the ScrapeOps app. |
| `html` | string | yes | The raw HTML to parse with the selected custom parser. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ScrapeOps API returns.

## Native endpoint

Through the native ScrapeOps API, this operation is `POST https://parser.scrapeops.io/v1/custom-parser` (base URL `http://headers.scrapeops.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-html-with-custom-parser.md) for the provider-specific parameters and requirements.

