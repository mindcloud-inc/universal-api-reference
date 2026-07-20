# Active Network: Get Asset By Guid

Retrieves an asset by GUID in Active Network.

```
GET https://connect.mindcloud.co/v1/universal/activeNetwork/latest/actions/get-asset-by-guid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Active Network `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeNetwork/latest/actions/get-asset-by-guid?connectionId=$CONNECTION_ID&assetGuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assetGuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activeNetwork/latest/actions/get-asset-by-guid?${params}`, {
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
| `assetGuid` | string | yes | Exact ACTIVE asset GUID to retrieve. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Active Network API returns.

## Native endpoint

Through the native Active Network API, this operation is `GET /v2/search` (base URL `http://api.amp.active.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asset-by-guid.md) for the provider-specific parameters and requirements.

