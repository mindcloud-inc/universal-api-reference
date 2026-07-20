# retailCRM: List Offers

Retrieves offers from retailCRM.

```
GET https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-offers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a retailCRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-offers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-offers?${params}`, {
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
      "active": true,
      "id": 1,
      "images": [
        "string"
      ],
      "name": "Ava Chen",
      "prices": [
        {
          "currency": "string",
          "ordering": 1,
          "price": 1,
          "priceType": "string"
        }
      ],
      "quantity": 1,
      "site": "string",
      "unit": {
        "code": "string",
        "name": "Ava Chen",
        "sym": "string"
      },
      "xmlId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `id` | number |  |
| `images` | array |  |
| `name` | string |  |
| `prices[].currency` | string |  |
| `prices[].ordering` | number |  |
| `prices[].price` | number |  |
| `prices[].priceType` | string |  |
| `quantity` | number |  |
| `site` | string |  |
| `unit.code` | string |  |
| `unit.name` | string |  |
| `unit.sym` | string |  |
| `xmlId` | string |  |

## Native endpoint

Through the native retailCRM API, this operation is `GET /store/offers` (base URL `{{credentials.accountUrl}}/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-offers.md) for the provider-specific parameters and requirements.

