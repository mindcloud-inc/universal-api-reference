# easybits Extractor: Extract Data

Extracts structured data from documents in easybits Extractor.

```
GET https://connect.mindcloud.co/v1/universal/easybitsExtractor/latest/actions/extract-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a easybits Extractor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easybitsExtractor/latest/actions/extract-data?connectionId=$CONNECTION_ID&files%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "files[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easybitsExtractor/latest/actions/extract-data?${params}`, {
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
| `files[]` | array<string> | yes | One or more document URLs or base64 data URLs to extract. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native easybits Extractor API returns.

## Native endpoint

Through the native easybits Extractor API, this operation is `POST /pipelines/:pipelineId` (base URL `https://extractor.easybits.tech/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-data.md) for the provider-specific parameters and requirements.

