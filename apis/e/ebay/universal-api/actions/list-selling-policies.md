# eBay: List Selling Policies

Retrieve a specific list of selling policies (i.e. fulfillment, payment & return policies)

```
GET https://connect.mindcloud.co/v1/universal/ebay/latest/actions/list-selling-policies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eBay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/list-selling-policies?connectionId=$CONNECTION_ID&marketplaceId=string&policy=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "marketplaceId": "string",
  "policy": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ebay/latest/actions/list-selling-policies?${params}`, {
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
| `marketplaceId` | string | yes | The eBay marketplace_id to retrieve the specified policies from. |
| `policy` | list<string> | yes | Specify which list of policies to retrieve. Accepted values are: payment, return, fulfillment, custom. |
| `policyTypes` | string<string> | no | (optional) parameter to be used only when retrieving "Custom" policies. Omitting this query parameter from a Custom Policies request will return all custom policies of all policy types. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native eBay API returns.

## Native endpoint

Through the native eBay API, this operation is `GET sell/account/v1/:policy/` (base URL `https://api.ebay.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-selling-policies.md) for the provider-specific parameters and requirements.

