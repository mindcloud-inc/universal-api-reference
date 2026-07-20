# Katana: Retrieve Current Factory

Retrieves the current factory from Katana.

```
GET https://connect.mindcloud.co/v1/universal/katana/latest/actions/retrieve-current-factory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/katana/latest/actions/retrieve-current-factory?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/katana/latest/actions/retrieve-current-factory?${params}`, {
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
      "baseCurrencyCode": "string",
      "defaultManufacturingLocationId": 1,
      "defaultPoLeadTime": "string",
      "defaultPurchasesLocationId": 1,
      "defaultSalesLocationId": 1,
      "defaultSoDeliveryTime": "string",
      "displayName": "Ava Chen",
      "inventoryClosingDate": "string",
      "legalAddress": {
        "city": "string",
        "country": "string",
        "line1": "string",
        "line2": "string",
        "state": "string",
        "zip": "string"
      },
      "legalName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseCurrencyCode` | string |  |
| `defaultManufacturingLocationId` | number |  |
| `defaultPoLeadTime` | string |  |
| `defaultPurchasesLocationId` | number |  |
| `defaultSalesLocationId` | number |  |
| `defaultSoDeliveryTime` | string |  |
| `displayName` | string |  |
| `inventoryClosingDate` | string |  |
| `legalAddress` | object |  |
| `legalAddress.city` | string |  |
| `legalAddress.country` | string |  |
| `legalAddress.line1` | string |  |
| `legalAddress.line2` | string |  |
| `legalAddress.state` | string |  |
| `legalAddress.zip` | string |  |
| `legalName` | string |  |

## Native endpoint

Through the native Katana API, this operation is `GET /factory` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-current-factory.md) for the provider-specific parameters and requirements.

