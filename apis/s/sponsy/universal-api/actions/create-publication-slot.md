# Sponsy: Create Publication Slot

Creates a publication slot in Sponsy.

```
POST https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/create-publication-slot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sponsy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/create-publication-slot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "publicationId": "string",
  "date": "string",
  "status": "string",
  "placement": "string",
  "content": "string",
  "price": 1,
  "customer": "string",
  "trackingNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/create-publication-slot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "publicationId": "string",
    "date": "string",
    "status": "string",
    "placement": "string",
    "content": "string",
    "price": 1,
    "customer": "string",
    "trackingNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `publicationId` | string | yes | Publication ID from Sponsy. |
| `date` | string | yes | Slot date in YYYY-MM-DD format. |
| `status` | string | yes | Publication status ID. |
| `placement` | string | yes | Publication placement ID. |
| `content` | string | yes | Slot ad copy content. |
| `price` | number | yes | Slot price. |
| `customer` | string | yes | Customer name. |
| `trackingNumber` | string | yes | Tracking number for the slot. |

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

Through the native Sponsy API, this operation is `POST /v1/publications/:publicationId/slots` (base URL `https://api.getsponsy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-publication-slot.md) for the provider-specific parameters and requirements.

