# AITable.ai: List Embedded Links

Retrieves embedded links for a node in AITable.ai.

```
GET https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/list-embedded-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AITable.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/list-embedded-links?connectionId=$CONNECTION_ID&spaceId=string&nodeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spaceId": "string",
  "nodeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/list-embedded-links?${params}`, {
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
| `spaceId` | string | yes | AITable space ID containing the node. |
| `nodeId` | string | yes | AITable node ID whose embedded links should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "embedLinks": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `embedLinks` | array<object> | Embedded links for the node. |

## Native endpoint

Through the native AITable.ai API, this operation is `GET /fusion/v1/spaces/:spaceId/nodes/:nodeId/embedlinks` (base URL `https://aitable.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-embedded-links.md) for the provider-specific parameters and requirements.

