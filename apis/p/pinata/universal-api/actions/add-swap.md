# Pinata: Add Swap

Updates a CID swap mapping in Pinata.

```
PUT https://connect.mindcloud.co/v1/universal/pinata/latest/actions/add-swap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pinata/latest/actions/add-swap" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cid": "string",
  "network": "string",
  "swapCid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinata/latest/actions/add-swap', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cid": "string",
    "network": "string",
    "swapCid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cid` | string | yes | Original CID to swap. |
| `network` | string | yes | Target network (`public` or `private`). |
| `swapCid` | string | yes | CID to redirect to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": {
        "code": 1,
        "message": "string",
        "reason": "string",
        "request": "string",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error.code` | number | Provider error code for the saved blocked run. |
| `error.message` | string | Provider error message. |
| `error.reason` | string | Provider error reason, when present. |
| `error.request` | string | Provider request identifier. |
| `error.status` | string | Provider error status. |

## Native endpoint

Through the native Pinata API, this operation is `PUT /v3/files/:network/swap/:cid` (base URL `https://api.pinata.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-swap.md) for the provider-specific parameters and requirements.

