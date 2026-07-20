# Dachser: Get Shipment History

Retrieves shipment history details from Dachser.

```
GET https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-shipment-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dachser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-shipment-history?connectionId=$CONNECTION_ID&trackingNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trackingNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-shipment-history?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | no | Optional customer ID. |
| `acceptLanguage` | string | no | Optional language sent as the Accept-Language header. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "consignee": {},
      "consignor": {},
      "forwarder": {},
      "id": "string",
      "references": [
        {}
      ],
      "shipmentDate": "2026-05-07T12:00:00.000Z",
      "shipments": [
        {}
      ],
      "shipmentWeight": {},
      "ssccs": [
        "string"
      ],
      "status": [
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
| `consignee` | object |  |
| `consignor` | object |  |
| `forwarder` | object |  |
| `id` | string |  |
| `references` | array<object> |  |
| `shipmentDate` | date |  |
| `shipments` | array<object> |  |
| `shipmentWeight` | object |  |
| `ssccs` | array<string> |  |
| `status` | array<object> |  |

## Native endpoint

Through the native Dachser API, this operation is `GET /rest/v2/shipmenthistory` (base URL `https://api-gateway.dachser.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shipment-history.md) for the provider-specific parameters and requirements.

