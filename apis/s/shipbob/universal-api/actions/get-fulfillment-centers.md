# ShipBob: Get Fulfillment Centers



```
GET https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/get-fulfillment-centers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShipBob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/get-fulfillment-centers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/get-fulfillment-centers?${params}`, {
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
      "address1": "string",
      "address2": "string",
      "city": "Ava Chen",
      "country": "string",
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "phoneNumber": "string",
      "state": "string",
      "timezone": "string",
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address1` | string |  |
| `address2` | string |  |
| `city` | string |  |
| `country` | string |  |
| `email` | string |  |
| `id` | number |  |
| `name` | string |  |
| `phoneNumber` | string |  |
| `state` | string |  |
| `timezone` | string |  |
| `zipCode` | string |  |

## Native endpoint

Through the native ShipBob API, this operation is `GET 1.0/fulfillmentCenter` (base URL `https://{{credentials.apiSubdomain}}.shipbob.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fulfillment-centers.md) for the provider-specific parameters and requirements.

