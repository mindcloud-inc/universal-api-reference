# Firecrawl: Start Agent

Creates an agent job in Firecrawl.

```
POST https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/start-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firecrawl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/start-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/start-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `urls[]` | array<string> | no | Optional list of URLs to constrain the agent to |
| `prompt` | string | yes | The prompt describing what data to extract |
| `schema` | object | no | Optional JSON schema to structure the extracted data |
| `maxCredits` | number | no | Maximum credits to spend on this agent task |
| `strictConstrainToURLs` | boolean | no | Only visit URLs provided in the urls array |
| `model` | string | no | The model to use for the agent task |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Firecrawl API, this operation is `POST /agent` (base URL `https://api.firecrawl.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-agent.md) for the provider-specific parameters and requirements.

