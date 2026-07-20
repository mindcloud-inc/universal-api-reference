# Bookvault: List Retailers

Retrieves available retailers from Bookvault.

```
GET https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-retailers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookvault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-retailers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-retailers?${params}`, {
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
      "Currency": "string",
      "IconImage": "string",
      "Name": "Ava Chen",
      "OrderPercentage": 1,
      "OrderRate": 1,
      "SoldAtDiscount": true,
      "StoreID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Currency` | string |  |
| `IconImage` | string |  |
| `Name` | string |  |
| `OrderPercentage` | number |  |
| `OrderRate` | number |  |
| `SoldAtDiscount` | boolean |  |
| `StoreID` | number |  |

## Native endpoint

Through the native Bookvault API, this operation is `GET /Retailers` (base URL `https://api.bookvault.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-retailers.md) for the provider-specific parameters and requirements.

