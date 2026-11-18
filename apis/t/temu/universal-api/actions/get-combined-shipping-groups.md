# Temu: Get Combined Shipping Groups

Retrieve combined shipping groups including lists of parent orders that can be combined for shipping.

```
GET https://connect.mindcloud.co/v1/universal/temu/latest/actions/get-combined-shipping-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Temu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/temu/latest/actions/get-combined-shipping-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/temu/latest/actions/get-combined-shipping-groups?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Temu API returns.

## Native endpoint

Through the native Temu API, this operation is `POST /router` (base URL `https://openapi-b-us.temu.com/openapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-combined-shipping-groups.md) for the provider-specific parameters and requirements.

