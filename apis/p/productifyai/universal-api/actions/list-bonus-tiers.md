# Productify.ai: List Bonus Tiers



```
GET https://connect.mindcloud.co/v1/universal/productifyai/latest/actions/list-bonus-tiers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productify.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productifyai/latest/actions/list-bonus-tiers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productifyai/latest/actions/list-bonus-tiers?${params}`, {
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
      "bonusTiers": [
        {}
      ],
      "description": "string",
      "heading": "string",
      "modelState": {},
      "wasSuccessful": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bonusTiers` | array<object> |  |
| `description` | string |  |
| `heading` | string |  |
| `modelState` | object |  |
| `wasSuccessful` | boolean |  |

## Native endpoint

Through the native Productify.ai API, this operation is `GET /pricing/bonus-tiers` (base URL `https://api.productify.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bonus-tiers.md) for the provider-specific parameters and requirements.

