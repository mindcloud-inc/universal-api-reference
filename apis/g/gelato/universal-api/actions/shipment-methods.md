# Gelato: Shipment Methods

Finds Gelato shipment methods by destination country.

```
GET https://connect.mindcloud.co/v1/universal/gelato/latest/actions/shipment-methods
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gelato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gelato/latest/actions/shipment-methods?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gelato/latest/actions/shipment-methods?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `country` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasTracking": true,
      "isBusiness": true,
      "isPrivate": true,
      "name": "Ava Chen",
      "shipmentMethodUid": "string",
      "supportedCountries": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasTracking` | boolean | Whether tracking is available. |
| `isBusiness` | boolean | Whether the method supports business recipients. |
| `isPrivate` | boolean | Whether the method supports private recipients. |
| `name` | string | Shipment method display name. |
| `shipmentMethodUid` | string | Gelato shipment method identifier. |
| `supportedCountries` | array<string> | Countries supported by the shipment method. |
| `type` | string | Shipment method type. |

## Native endpoint

Through the native Gelato API, this operation is `GET https://shipment.gelatoapis.com/v1/shipment-methods` (base URL `https://order.gelatoapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/shipment-methods.md) for the provider-specific parameters and requirements.

