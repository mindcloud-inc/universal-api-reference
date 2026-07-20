# MindStudio: Generate Signed Access URL

Creates a signed access URL for a MindStudio agent.

```
POST https://connect.mindcloud.co/v1/universal/mindStudio/latest/actions/generate-signed-access-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MindStudio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mindStudio/latest/actions/generate-signed-access-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mindStudio/latest/actions/generate-signed-access-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes | The MindStudio agent ID to generate a signed access URL for. |
| `userId` | string | no | Optional unique user identifier for the signed access session. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string | The signed access URL for the requested agent. |

## Native endpoint

Through the native MindStudio API, this operation is `POST /generate-signed-access-url` (base URL `https://api.mindstudio.ai/developer/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-signed-access-url.md) for the provider-specific parameters and requirements.

