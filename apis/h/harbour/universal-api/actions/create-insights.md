# Harbour: Create Insights

Creates document insights from completed documents, drafts, or URLs in Harbour.

```
POST https://connect.mindcloud.co/v1/universal/harbour/latest/actions/create-insights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harbour `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/harbour/latest/actions/create-insights" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "context": "string",
  "insights[]": [
    {}
  ],
  "stream": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harbour/latest/actions/create-insights', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "context": "string",
    "insights[]": [{}],
    "stream": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `draft_id` | string | no | Harbour draft document identifier. Provide one of draft_id, completed_id, doc_text, or url. |
| `completed_id` | string | no | Harbour completed agreement asset identifier. Provide one of draft_id, completed_id, doc_text, or url. |
| `doc_text` | string | no | Raw document text to analyze. Provide one of draft_id, completed_id, doc_text, or url. |
| `url` | string | no | Publicly accessible document URL to analyze. Provide one of draft_id, completed_id, doc_text, or url. |
| `context` | string | yes | Background context the model can use while generating insights. |
| `insights[]` | array<object> | yes | List of Harbour insight request objects, for example [{ "type": "document_title" }, { "type": "contract_values" }]. |
| `stream` | boolean | yes | Whether Harbour should stream the insight generation response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "insight": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `insight` | object |  |

## Native endpoint

Through the native Harbour API, this operation is `POST /insights` (base URL `https://api.myharbourshare.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-insights.md) for the provider-specific parameters and requirements.

