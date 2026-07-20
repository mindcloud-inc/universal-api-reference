# Productify.ai: List Operation Costs



```
GET https://connect.mindcloud.co/v1/universal/productifyai/latest/actions/list-operation-costs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productify.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productifyai/latest/actions/list-operation-costs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productifyai/latest/actions/list-operation-costs?${params}`, {
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
      "batches": [
        {}
      ],
      "description": "string",
      "heading": "string",
      "modelState": {},
      "translationAdditionalCost": 1,
      "wasSuccessful": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batches` | array<object> |  |
| `description` | string |  |
| `heading` | string |  |
| `modelState` | object |  |
| `translationAdditionalCost` | number |  |
| `wasSuccessful` | boolean |  |

## Native endpoint

Through the native Productify.ai API, this operation is `GET /pricing/operation-costs` (base URL `https://api.productify.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-operation-costs.md) for the provider-specific parameters and requirements.

