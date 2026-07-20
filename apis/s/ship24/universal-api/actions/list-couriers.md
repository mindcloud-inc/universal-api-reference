# Ship24: List Couriers

Retrieves all available couriers from Ship24.

```
GET https://connect.mindcloud.co/v1/universal/ship24/latest/actions/list-couriers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ship24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ship24/latest/actions/list-couriers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ship24/latest/actions/list-couriers?${params}`, {
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
      "countryCode": {},
      "courierCode": "string",
      "courierName": "Ava Chen",
      "isDeprecated": true,
      "isPost": true,
      "requiredFields": {},
      "website": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countryCode` | object |  |
| `courierCode` | string |  |
| `courierName` | string |  |
| `isDeprecated` | boolean |  |
| `isPost` | boolean |  |
| `requiredFields` | object |  |
| `website` | object |  |

## Native endpoint

Through the native Ship24 API, this operation is `GET /public/v1/couriers` (base URL `https://api.ship24.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-couriers.md) for the provider-specific parameters and requirements.

