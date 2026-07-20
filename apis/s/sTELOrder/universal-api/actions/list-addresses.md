# STEL Order: List Addresses

Retrieves a list of addresses from STEL Order.

```
GET https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a STEL Order `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-addresses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-addresses?${params}`, {
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
      "account-id": 1,
      "account-path": "string",
      "address-data": "string",
      "address-type": "string",
      "city-town": "string",
      "country-code": "string",
      "deleted": true,
      "id": 1,
      "path": "string",
      "postal-code": "string",
      "province": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account-id` | number |  |
| `account-path` | string |  |
| `address-data` | string |  |
| `address-type` | string |  |
| `city-town` | string |  |
| `country-code` | string |  |
| `deleted` | boolean |  |
| `id` | number |  |
| `path` | string |  |
| `postal-code` | string |  |
| `province` | string |  |

## Native endpoint

Through the native STEL Order API, this operation is `GET /addresses` (base URL `https://app.stelorder.com/app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-addresses.md) for the provider-specific parameters and requirements.

