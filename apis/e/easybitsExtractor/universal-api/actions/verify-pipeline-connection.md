# easybits Extractor: Verify Pipeline Connection

Verifies a pipeline connection in easybits Extractor.

```
GET https://connect.mindcloud.co/v1/universal/easybitsExtractor/latest/actions/verify-pipeline-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a easybits Extractor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easybitsExtractor/latest/actions/verify-pipeline-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easybitsExtractor/latest/actions/verify-pipeline-connection?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean | True when the configured pipeline ID and API key are accepted by Easybits Extractor. |

## Native endpoint

Through the native easybits Extractor API, this operation is `GET /pipelines/:pipelineId/test` (base URL `https://extractor.easybits.tech/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-pipeline-connection.md) for the provider-specific parameters and requirements.

