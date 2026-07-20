# Ventrata: List Products

Retrieves products from Ventrata.

```
GET https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ventrata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/list-products?${params}`, {
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
      "allowFreesale": true,
      "availabilityRequired": true,
      "availabilityType": "string",
      "deliveryFormats": [
        "string"
      ],
      "deliveryMethods": [
        "string"
      ],
      "id": "string",
      "instantConfirmation": true,
      "instantDelivery": true,
      "internalName": "Ava Chen",
      "locale": "string",
      "options": [
        {
          "availabilityLocalDateStart": "2026-05-07T12:00:00.000Z",
          "availabilityLocalStartTimes": [
            "string"
          ],
          "default": true,
          "id": "string",
          "internalName": "Ava Chen",
          "units": [
            {
              "id": "string",
              "internalName": "Ava Chen",
              "type": "string"
            }
          ]
        }
      ],
      "redemptionMethod": "string",
      "settlementMethods": [
        "string"
      ],
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowFreesale` | boolean |  |
| `availabilityRequired` | boolean |  |
| `availabilityType` | string |  |
| `deliveryFormats[]` | string |  |
| `deliveryMethods[]` | string |  |
| `id` | string |  |
| `instantConfirmation` | boolean |  |
| `instantDelivery` | boolean |  |
| `internalName` | string |  |
| `locale` | string |  |
| `options[].availabilityLocalDateStart` | date |  |
| `options[].availabilityLocalStartTimes[]` | string |  |
| `options[].default` | boolean |  |
| `options[].id` | string |  |
| `options[].internalName` | string |  |
| `options[].units[].id` | string |  |
| `options[].units[].internalName` | string |  |
| `options[].units[].type` | string |  |
| `redemptionMethod` | string |  |
| `settlementMethods[]` | string |  |
| `timeZone` | string |  |

## Native endpoint

Through the native Ventrata API, this operation is `GET octo/products` (base URL `https://api.ventrata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

