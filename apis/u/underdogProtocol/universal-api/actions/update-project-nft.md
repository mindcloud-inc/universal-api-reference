# Underdog Protocol: Update Project NFT

Updates an existing project NFT in Underdog Protocol.

```
PUT https://connect.mindcloud.co/v1/universal/underdogProtocol/latest/actions/update-project-nft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Underdog Protocol `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/underdogProtocol/latest/actions/update-project-nft" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transferable": "n",
  "projectId": 1,
  "nftId": 1,
  "image": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/underdogProtocol/latest/actions/update-project-nft', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transferable": "n",
    "projectId": 1,
    "nftId": 1,
    "image": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transferable` | list | yes | Value must be either 't' for transferable or 'n' for non-transferable One of: `n`, `t`. |
| `projectId` | number | yes |  |
| `nftId` | number | yes |  |
| `description` | string | no | Description stored in the metadata |
| `image` | string | yes | Image URL for your NFT |
| `attributes` | object | no | Key-value pairs of your NFT attributes |
| `animationUrl` | string | no | Animation URL for your NFT |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Underdog Protocol API returns.

## Native endpoint

Through the native Underdog Protocol API, this operation is `PUT /v2/projects/:transferable/:projectId/nfts/:nftId` (base URL `https://dev.underdogprotocol.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project-nft.md) for the provider-specific parameters and requirements.

