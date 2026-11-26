# eBay: Delete Offer



```
DELETE https://connect.mindcloud.co/v1/universal/ebay/latest/actions/delete-offer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eBay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/delete-offer?connectionId=$CONNECTION_ID&offerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "offerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ebay/latest/actions/delete-offer?${params}`, {
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
| `offerId` | string | yes | The unique identifier of the offer being deleted. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native eBay API returns.

## Native endpoint

Through the native eBay API, this operation is `DELETE sell/inventory/v1/offer/:offerId` (base URL `https://api.ebay.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-offer.md) for the provider-specific parameters and requirements.

