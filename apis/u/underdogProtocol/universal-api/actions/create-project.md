# Underdog Protocol: Create Project

Creates a new project in Underdog Protocol.

```
POST https://connect.mindcloud.co/v1/universal/underdogProtocol/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Underdog Protocol `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/underdogProtocol/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "image": "string",
  "transferable": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/underdogProtocol/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "image": "string",
    "transferable": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name stored as on-chain metadata |
| `symbol` | string | no | Symbol stored as on-chain metadata |
| `description` | string | no | Description stored in the metadata |
| `image` | string | yes | Image URL for your NFT |
| `transferable` | boolean | yes | Whether or not the NFTs in this project can be transferred |
| `animationUrl` | string | no | Animation URL for your NFT |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Underdog Protocol API returns.

## Native endpoint

Through the native Underdog Protocol API, this operation is `POST /v2/projects` (base URL `https://dev.underdogprotocol.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

