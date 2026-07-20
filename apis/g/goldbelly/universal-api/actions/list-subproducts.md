# Goldbelly: List Subproducts



```
GET https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/list-subproducts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goldbelly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/list-subproducts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/list-subproducts?${params}`, {
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
      "inventory": 1,
      "inventorySold": 1,
      "name": "Ava Chen",
      "sku": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inventory` | number |  |
| `inventorySold` | number |  |
| `name` | string |  |
| `sku` | string |  |

## Native endpoint

Through the native Goldbelly API, this operation is `GET subproducts` (base URL `https://api.goldbelly.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subproducts.md) for the provider-specific parameters and requirements.

