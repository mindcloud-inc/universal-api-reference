# Sponsy: List Customer Slots

Retrieves customer slots from Sponsy.

```
GET https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/list-customer-slots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sponsy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/list-customer-slots?connectionId=$CONNECTION_ID&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/list-customer-slots?${params}`, {
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
| `customerId` | string | yes | Customer ID from Sponsy. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clicks": 1,
      "ctor": 1,
      "ctr": 1,
      "currentPrice": 1,
      "date": "string",
      "hasAssets": true,
      "hasMetrics": true,
      "id": "string",
      "openRate": 1,
      "placementId": "string",
      "price": 1,
      "priceType": "string",
      "publicationId": "string",
      "tctor": 1,
      "tctr": 1,
      "totalOpens": 1,
      "totalSends": 1,
      "trackingNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clicks` | number |  |
| `ctor` | number |  |
| `ctr` | number |  |
| `currentPrice` | number |  |
| `date` | string |  |
| `hasAssets` | boolean |  |
| `hasMetrics` | boolean |  |
| `id` | string |  |
| `openRate` | number |  |
| `placementId` | string |  |
| `price` | number |  |
| `priceType` | string |  |
| `publicationId` | string |  |
| `tctor` | number |  |
| `tctr` | number |  |
| `totalOpens` | number |  |
| `totalSends` | number |  |
| `trackingNumber` | string |  |

## Native endpoint

Through the native Sponsy API, this operation is `GET /v1/customers/:customerId/slots` (base URL `https://api.getsponsy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-slots.md) for the provider-specific parameters and requirements.

