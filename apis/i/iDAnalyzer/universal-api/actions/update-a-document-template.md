# ID Analyzer: Update a document template

Updates a document template in ID Analyzer.

```
PUT https://connect.mindcloud.co/v1/universal/iDAnalyzer/latest/actions/update-a-document-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ID Analyzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/iDAnalyzer/latest/actions/update-a-document-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string",
  "name": "Ava Chen",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iDAnalyzer/latest/actions/update-a-document-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string",
    "name": "Ava Chen",
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | yes | Updated HTML template content. |
| `name` | string | yes | Template name required by the provider when updating template content. |
| `templateId` | string | yes | Stored template ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ID Analyzer API returns.

## Native endpoint

Through the native ID Analyzer API, this operation is `POST /contract/:templateId` (base URL `https://api2.idanalyzer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-document-template.md) for the provider-specific parameters and requirements.

