# Copperx: Get Price

Retrieves price record details from Copperx.

```
GET https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-price
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Copperx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-price?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-price?${params}`, {
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
| `id` | string | yes | Price ID path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingScheme": "string",
      "createdAt": "string",
      "currency": "string",
      "customPreset": "string",
      "customUnitAmountSuggestions": [
        "string"
      ],
      "customUnitMax": "string",
      "customUnitMin": "string",
      "id": "string",
      "interval": "string",
      "intervalCount": 1,
      "isActive": true,
      "metadata": {},
      "product": {},
      "productId": "string",
      "type": "string",
      "unitAmount": "string",
      "unitAmountDecimal": "string",
      "updatedAt": "string",
      "usageType": "string",
      "visibility": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingScheme` | string |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `customPreset` | string |  |
| `customUnitAmountSuggestions` | array<string> |  |
| `customUnitMax` | string |  |
| `customUnitMin` | string |  |
| `id` | string |  |
| `interval` | string |  |
| `intervalCount` | number |  |
| `isActive` | boolean |  |
| `metadata` | object |  |
| `product` | object |  |
| `productId` | string |  |
| `type` | string |  |
| `unitAmount` | string |  |
| `unitAmountDecimal` | string |  |
| `updatedAt` | string |  |
| `usageType` | string |  |
| `visibility` | number |  |

## Native endpoint

Through the native Copperx API, this operation is `GET /prices/{id}` (base URL `https://api.copperx.dev/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-price.md) for the provider-specific parameters and requirements.

