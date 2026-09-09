# Walmart: Get Shipping Configurations

Retrieve shipping configurations like Lag Time.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-shipping-configurations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-shipping-configurations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-shipping-configurations?${params}`, {
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
      "configurations": [
        {
          "configurationName": "Ava Chen"
        }
      ],
      "partner": {
        "partnerDisplayName": "Ava Chen",
        "partnerId": "string",
        "partnerName": "Ava Chen",
        "partnerStoreId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configurations[].configurationName` | string |  |
| `partner.partnerDisplayName` | string |  |
| `partner.partnerId` | string |  |
| `partner.partnerName` | string |  |
| `partner.partnerStoreId` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/settings/shippingprofile` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shipping-configurations.md) for the provider-specific parameters and requirements.

