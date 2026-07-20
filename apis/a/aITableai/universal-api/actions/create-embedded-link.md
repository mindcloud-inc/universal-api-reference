# AITable.ai: Create Embedded Link

Creates a new embedded link in AITable.ai.

```
POST https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/create-embedded-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AITable.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/create-embedded-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spaceId": "string",
  "nodeId": "string",
  "payload": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/create-embedded-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spaceId": "string",
    "nodeId": "string",
    "payload": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `spaceId` | string | yes | AITable space ID containing the node. |
| `nodeId` | string | yes | AITable node ID for the embedded link. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payload` | object | yes | Embedded link request body from AITable. Use the fields required by the AITable embedded link endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "linkId": "https://example.com",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `linkId` | string | Created embedded link ID. |
| `url` | string | Embedded link URL. |

## Native endpoint

Through the native AITable.ai API, this operation is `POST /fusion/v1/spaces/:spaceId/nodes/:nodeId/embedlinks` (base URL `https://aitable.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-embedded-link.md) for the provider-specific parameters and requirements.

