# Agiliron: Read PurchaseOrder

Retrieves purchase order records from Agiliron.

```
GET https://connect.mindcloud.co/v1/universal/agiliron/latest/actions/read-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agiliron `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agiliron/latest/actions/read-purchase-order?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agiliron/latest/actions/read-purchase-order?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Agiliron API returns.

## Native endpoint

Through the native Agiliron API, this operation is `GET PurchaseOrder` (base URL `https://{{credentials.yourCompany}}.agiliron.net/agiliron/api-40.php/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-purchase-order.md) for the provider-specific parameters and requirements.

