# Shopia: Generate Article Ideas



```
POST https://connect.mindcloud.co/v1/universal/shopia/latest/actions/generate-article-ideas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shopia/latest/actions/generate-article-ideas" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "topic": "Productivity workflows",
  "audience": "SaaS founders"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shopia/latest/actions/generate-article-ideas', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "topic": "Productivity workflows",
    "audience": "SaaS founders"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `topic` | string | yes | The topic to generate article ideas about. Example: `Productivity workflows`. |
| `audience` | string | yes | The target audience for the article ideas. Example: `SaaS founders`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "outputs": [
        "string"
      ],
      "outputsPlainText": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `outputs` | array<string> | HTML-formatted article ideas returned by the Shopia automation. |
| `outputsPlainText` | array<string> | Plain-text article ideas returned by the Shopia automation. |

## Native endpoint

Through the native Shopia API, this operation is `POST https://automation-run-1he1fvca.uc.gateway.dev/automation?key={{credentials.apiKey}}&token={{credentials.token}}&workflow={{credentials.workflowId}}` (base URL `https://automation-run-1he1fvca.uc.gateway.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-article-ideas.md) for the provider-specific parameters and requirements.

