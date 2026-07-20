# Active Network: Get Asset By Exact Name

Retrieves an asset by exact name in Active Network.

```
GET https://connect.mindcloud.co/v1/universal/activeNetwork/latest/actions/get-asset-by-exact-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Active Network `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeNetwork/latest/actions/get-asset-by-exact-name?connectionId=$CONNECTION_ID&assetName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assetName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activeNetwork/latest/actions/get-asset-by-exact-name?${params}`, {
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
| `assetName` | string | yes | Exact ACTIVE asset name to retrieve. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Active Network API returns.

## Native endpoint

Through the native Active Network API, this operation is `GET /v2/search` (base URL `http://api.amp.active.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asset-by-exact-name.md) for the provider-specific parameters and requirements.

