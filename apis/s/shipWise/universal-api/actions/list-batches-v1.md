# ShipWise: List Batches V1

Retrieves batches from ShipWise.

```
GET https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/list-batches-v1
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShipWise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/list-batches-v1?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/list-batches-v1?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ShipWise API returns.

## Native endpoint

Through the native ShipWise API, this operation is `GET /api/v1/Batch` (base URL `https://api.shipwise.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-batches-v1.md) for the provider-specific parameters and requirements.

