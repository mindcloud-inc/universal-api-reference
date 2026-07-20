# Dachser: Get Proofs Of Delivery

Retrieves proofs of delivery from Dachser.

```
GET https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-proofs-of-delivery
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dachser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-proofs-of-delivery?connectionId=$CONNECTION_ID&trackingNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trackingNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-proofs-of-delivery?${params}`, {
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
| `trackingNumber` | string | yes | Shipment tracking number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documents": [
        {}
      ],
      "id": "string",
      "links": [
        {}
      ],
      "references": [
        {}
      ],
      "shipmentDate": "2026-05-07T12:00:00.000Z",
      "shipments": [
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
| `documents` | array<object> |  |
| `id` | string |  |
| `links` | array<object> |  |
| `references` | array<object> |  |
| `shipmentDate` | date |  |
| `shipments` | array<object> |  |

## Native endpoint

Through the native Dachser API, this operation is `GET /rest/v2/pods` (base URL `https://api-gateway.dachser.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-proofs-of-delivery.md) for the provider-specific parameters and requirements.

