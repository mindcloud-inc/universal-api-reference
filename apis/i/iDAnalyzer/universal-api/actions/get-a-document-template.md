# ID Analyzer: Get a document template

Retrieves a document template from ID Analyzer.

```
GET https://connect.mindcloud.co/v1/universal/iDAnalyzer/latest/actions/get-a-document-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ID Analyzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iDAnalyzer/latest/actions/get-a-document-template?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iDAnalyzer/latest/actions/get-a-document-template?${params}`, {
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
| `templateId` | string | yes | Stored template ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ID Analyzer API returns.

## Native endpoint

Through the native ID Analyzer API, this operation is `GET /contract/:templateId` (base URL `https://api2.idanalyzer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-document-template.md) for the provider-specific parameters and requirements.

