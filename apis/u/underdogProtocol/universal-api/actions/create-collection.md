# Underdog Protocol: Create Collection

Creates a new collection in Underdog Protocol.

```
POST https://connect.mindcloud.co/v1/universal/underdogProtocol/latest/actions/create-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Underdog Protocol `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/underdogProtocol/latest/actions/create-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "description": "string",
  "image": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/underdogProtocol/latest/actions/create-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "description": "string",
    "image": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name for you NFT Collection |
| `description` | string | yes | Description for your NFT Collection |
| `image` | string | yes | URL pointing to an image for your NFT Collection |
| `attributes` | object | no | Key-value pairs where the key is the attribute name and the value is the attribute value. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Underdog Protocol API returns.

## Native endpoint

Through the native Underdog Protocol API, this operation is `POST /v1/collections` (base URL `https://dev.underdogprotocol.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-collection.md) for the provider-specific parameters and requirements.

