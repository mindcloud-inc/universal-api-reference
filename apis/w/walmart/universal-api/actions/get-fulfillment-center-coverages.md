# Walmart: Get Fulfillment Center Coverages

This API provides the list of all fullfillment centers for the seller and their coverage areas defined by Walmart based on the address.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-fulfillment-center-coverages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-fulfillment-center-coverages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-fulfillment-center-coverages?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "coverageArea": [
        "string"
      ],
      "shipNode": "string",
      "shipNodeName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `coverageArea[]` | string |  |
| `shipNode` | string |  |
| `shipNodeName` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/settings/shipping/shipnodes/coverage` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fulfillment-center-coverages.md) for the provider-specific parameters and requirements.

