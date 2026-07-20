# Pinata: Get Swap History

Retrieves CID swap history from Pinata.

```
GET https://connect.mindcloud.co/v1/universal/pinata/latest/actions/get-swap-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinata/latest/actions/get-swap-history?connectionId=$CONNECTION_ID&cid=string&domain=string&network=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cid": "string",
  "domain": "string",
  "network": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinata/latest/actions/get-swap-history?${params}`, {
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
| `cid` | string | yes | Original CID to inspect. |
| `domain` | string | yes | Gateway domain with the Hot Swaps plugin installed. |
| `network` | string | yes | Target network (`public` or `private`). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "mapped_cid": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].created_at` | date |  |
| `data[].mapped_cid` | string |  |

## Native endpoint

Through the native Pinata API, this operation is `GET /v3/files/:network/swap/:cid` (base URL `https://api.pinata.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-swap-history.md) for the provider-specific parameters and requirements.

