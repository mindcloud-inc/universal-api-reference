# Pinata: Remove Swap

Deletes an existing CID swap from Pinata.

```
DELETE https://connect.mindcloud.co/v1/universal/pinata/latest/actions/remove-swap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pinata/latest/actions/remove-swap?connectionId=$CONNECTION_ID&cid=string&network=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cid": "string",
  "network": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinata/latest/actions/remove-swap?${params}`, {
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
| `cid` | string | yes | Original CID whose swap should be removed. |
| `network` | string | yes | Target network (`public` or `private`). |

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

Through the native Pinata API, this operation is `DELETE /v3/files/:network/swap/:cid` (base URL `https://api.pinata.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-swap.md) for the provider-specific parameters and requirements.

