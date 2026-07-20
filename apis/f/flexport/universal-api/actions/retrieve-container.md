# Flexport: Retrieve Container

Retrieves a container from your Flexport account.

```
GET https://connect.mindcloud.co/v1/universal/flexport/latest/actions/retrieve-container
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexport `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexport/latest/actions/retrieve-container?connectionId=$CONNECTION_ID&id=12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flexport/latest/actions/retrieve-container?${params}`, {
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
| `id` | number | yes | Unique Flexport ocean shipment container ID to retrieve. Example: `12345`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actualArrivalDate": "2026-05-07T12:00:00.000Z",
      "actualDeliveryDate": "2026-05-07T12:00:00.000Z",
      "actualDepartureDate": "2026-05-07T12:00:00.000Z",
      "actualPickupDate": "2026-05-07T12:00:00.000Z",
      "availableForPickupDate": "2026-05-07T12:00:00.000Z",
      "cargoReadyDate": "2026-05-07T12:00:00.000Z",
      "containerLegs": {},
      "containerNumber": "string",
      "containerSize": "string",
      "containerType": "string",
      "emptyContainerPickupDate": "2026-05-07T12:00:00.000Z",
      "emptyReadyDate": "2026-05-07T12:00:00.000Z",
      "emptyReturnedDate": "2026-05-07T12:00:00.000Z",
      "estimatedArrivalDate": "2026-05-07T12:00:00.000Z",
      "estimatedAvailableForPickupDate": "2026-05-07T12:00:00.000Z",
      "estimatedDeliveryDate": "2026-05-07T12:00:00.000Z",
      "estimatedDepartureDate": "2026-05-07T12:00:00.000Z",
      "estimatedPickupDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "items": [
        {}
      ],
      "lastFreeDayDate": "2026-05-07T12:00:00.000Z",
      "metadata": {},
      "pickupNumber": "string",
      "referenceCode": "string",
      "sealNumber": "string",
      "shipment": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actualArrivalDate` | date |  |
| `actualDeliveryDate` | date |  |
| `actualDepartureDate` | date |  |
| `actualPickupDate` | date |  |
| `availableForPickupDate` | date |  |
| `cargoReadyDate` | date |  |
| `containerLegs` | object |  |
| `containerNumber` | string |  |
| `containerSize` | string |  |
| `containerType` | string |  |
| `emptyContainerPickupDate` | date |  |
| `emptyReadyDate` | date |  |
| `emptyReturnedDate` | date |  |
| `estimatedArrivalDate` | date |  |
| `estimatedAvailableForPickupDate` | date |  |
| `estimatedDeliveryDate` | date |  |
| `estimatedDepartureDate` | date |  |
| `estimatedPickupDate` | date |  |
| `id` | number |  |
| `items` | array<object> |  |
| `lastFreeDayDate` | date |  |
| `metadata` | object |  |
| `pickupNumber` | string |  |
| `referenceCode` | string |  |
| `sealNumber` | string |  |
| `shipment` | object |  |

## Native endpoint

Through the native Flexport API, this operation is `GET /ocean/shipment_containers/:id` (base URL `https://api.flexport.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-container.md) for the provider-specific parameters and requirements.

