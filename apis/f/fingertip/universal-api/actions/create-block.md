# Fingertip: Create Block



```
POST https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/create-block
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fingertip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/create-block" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageId": "string",
  "name": "Ava Chen",
  "kind": "string",
  "componentBlockId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/create-block', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageId": "string",
    "name": "Ava Chen",
    "kind": "string",
    "componentBlockId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageId` | string | yes | ID of the page to create a block in |
| `name` | string | yes | Name of the block |
| `kind` | string | yes | Type or category of the block |
| `componentBlockId` | string | yes | ID of the component block if this is an instance |
| `isComponent` | boolean | no | Whether this block is a component |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | object | no | Content of the block |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fingertip API returns.

## Native endpoint

Through the native Fingertip API, this operation is `POST /v1/pages/:pageId/blocks` (base URL `https://api.fingertip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-block.md) for the provider-specific parameters and requirements.

