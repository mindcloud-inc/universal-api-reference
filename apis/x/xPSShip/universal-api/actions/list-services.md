# XPS Ship: List Services

Retrieves shipping services from XPS Ship.

```
GET https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/list-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XPS Ship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/list-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/list-services?${params}`, {
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
      "carrierCode": "string",
      "carrierLabel": "string",
      "inbound": true,
      "packageTypes": [
        {}
      ],
      "serviceCode": "string",
      "serviceLabel": "string",
      "services": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrierCode` | string |  |
| `carrierLabel` | string |  |
| `inbound` | boolean |  |
| `packageTypes` | array<object> |  |
| `serviceCode` | string |  |
| `serviceLabel` | string |  |
| `services` | array<object> | Available services and package types. |

## Native endpoint

Through the native XPS Ship API, this operation is `GET /restapi/v1/customers/:customerId/services` (base URL `https://xpsshipper.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-services.md) for the provider-specific parameters and requirements.

