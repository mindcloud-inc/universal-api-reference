# Emporix Commerce Engine: Get Price List

Retrieves a price list from Emporix Commerce Engine.

```
GET https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-price-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emporix Commerce Engine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-price-list?connectionId=$CONNECTION_ID&priceListId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "priceListId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-price-list?${params}`, {
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
| `priceListId` | string | yes | The unique ID of the price list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "countries": [
        "string"
      ],
      "currency": "string",
      "customerGroups": [
        {}
      ],
      "id": "string",
      "legalEntityId": "string",
      "metadata": {},
      "name": {},
      "regions": [
        "string"
      ],
      "siteCode": "string",
      "validity": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countries` | array<string> |  |
| `currency` | string |  |
| `customerGroups` | array<object> |  |
| `id` | string |  |
| `legalEntityId` | string |  |
| `metadata` | object |  |
| `name` | object |  |
| `regions` | array<string> |  |
| `siteCode` | string |  |
| `validity` | object |  |

## Native endpoint

Through the native Emporix Commerce Engine API, this operation is `GET /price/{{credentials.tenantId}}/price-lists/:priceListId` (base URL `https://api.emporix.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-price-list.md) for the provider-specific parameters and requirements.

