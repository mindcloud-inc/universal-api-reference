# Dachser: Get Freight Costs

Retrieves freight costs for a consignment from Dachser.

```
GET https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-freight-costs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dachser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-freight-costs?connectionId=$CONNECTION_ID&trackingNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trackingNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-freight-costs?${params}`, {
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
| `acceptLanguage` | string | no | Optional language sent as the Accept-Language header. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "consignee": {},
      "consignor": {},
      "costs": {},
      "forwarder": {},
      "id": "string",
      "references": [
        {}
      ],
      "shipmentDate": "2026-05-07T12:00:00.000Z",
      "shipmentLoadMetres": 1,
      "shipmentVolume": {},
      "shipmentWeight": {}
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
| `costs` | object |  |
| `forwarder` | object |  |
| `id` | string |  |
| `references` | array<object> |  |
| `shipmentDate` | date |  |
| `shipmentLoadMetres` | number |  |
| `shipmentVolume` | object |  |
| `shipmentWeight` | object |  |

## Native endpoint

Through the native Dachser API, this operation is `GET /rest/v2/freightcosts` (base URL `https://api-gateway.dachser.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-freight-costs.md) for the provider-specific parameters and requirements.

