# Melo: List Searches

Retrieves existing searches from Melo matching the current criteria.

```
GET https://connect.mindcloud.co/v1/universal/melo/latest/actions/list-searches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Melo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/melo/latest/actions/list-searches?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/melo/latest/actions/list-searches?${params}`, {
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
| `page` | number | no | Collection page number. Default: `1`. |
| `itemsPerPage` | number | no | Number of items per page. Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "advertPriceMax": {},
      "advertPriceMin": {},
      "bedroomMin": 1,
      "budgetMax": 1,
      "budgetMin": 1,
      "createdAt": "string",
      "endpointRecipient": "string",
      "eventEndpoint": "string",
      "furnished": {},
      "geoShapes": {},
      "hidePropertyContact": true,
      "initiatedFromDashboard": true,
      "landSurfaceMax": {},
      "landSurfaceMin": {},
      "lastAlertAt": {},
      "lat": 1,
      "lon": 1,
      "notificationEnabled": true,
      "notificationRecipient": "string",
      "pricePerMeterMax": {},
      "pricePerMeterMin": {},
      "propertyTypes": [
        1
      ],
      "radius": 1,
      "roomMin": {},
      "subscribedEvents": [
        "string"
      ],
      "surfaceMax": 1,
      "surfaceMin": 1,
      "title": "string",
      "token": "string",
      "transactionType": 1,
      "updatedAt": "string",
      "user": "string",
      "withCoherentPrice": true,
      "withVirtualTour": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `advertPriceMax` | object |  |
| `advertPriceMin` | object |  |
| `bedroomMin` | number |  |
| `budgetMax` | number |  |
| `budgetMin` | number |  |
| `createdAt` | string |  |
| `endpointRecipient` | string |  |
| `eventEndpoint` | string |  |
| `furnished` | object |  |
| `geoShapes` | object |  |
| `hidePropertyContact` | boolean |  |
| `initiatedFromDashboard` | boolean |  |
| `landSurfaceMax` | object |  |
| `landSurfaceMin` | object |  |
| `lastAlertAt` | object |  |
| `lat` | number |  |
| `lon` | number |  |
| `notificationEnabled` | boolean |  |
| `notificationRecipient` | string |  |
| `pricePerMeterMax` | object |  |
| `pricePerMeterMin` | object |  |
| `propertyTypes[]` | number |  |
| `radius` | number |  |
| `roomMin` | object |  |
| `subscribedEvents[]` | string |  |
| `surfaceMax` | number |  |
| `surfaceMin` | number |  |
| `title` | string |  |
| `token` | string |  |
| `transactionType` | number |  |
| `updatedAt` | string |  |
| `user` | string |  |
| `withCoherentPrice` | boolean |  |
| `withVirtualTour` | object |  |

## Native endpoint

Through the native Melo API, this operation is `GET /searches` (base URL `https://preprod-api.notif.immo`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-searches.md) for the provider-specific parameters and requirements.

