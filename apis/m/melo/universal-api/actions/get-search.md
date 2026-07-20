# Melo: Get Search

Retrieves details for an existing search from Melo.

```
GET https://connect.mindcloud.co/v1/universal/melo/latest/actions/get-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Melo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/melo/latest/actions/get-search?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/melo/latest/actions/get-search?${params}`, {
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
| `id` | string | yes | Search resource identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "advertPriceMax": {},
      "advertPriceMin": {},
      "bedroomMin": {},
      "budgetMax": 1,
      "budgetMin": {},
      "createdAt": "string",
      "endpointRecipient": {},
      "eventEndpoint": {},
      "furnished": {},
      "geoShapes": {},
      "hidePropertyContact": true,
      "includedDepartments": [
        {
          "chefLieu": "string",
          "departmentCode": "string",
          "name": "Ava Chen",
          "nameClean": "Ava Chen"
        }
      ],
      "initiatedFromDashboard": true,
      "landSurfaceMax": {},
      "landSurfaceMin": {},
      "lastAlertAt": {},
      "lat": {},
      "lon": {},
      "notificationEnabled": true,
      "notificationRecipient": {},
      "pricePerMeterMax": {},
      "pricePerMeterMin": {},
      "propertyTypes": [
        1
      ],
      "radius": {},
      "roomMin": {},
      "surfaceMax": {},
      "surfaceMin": {},
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
| `bedroomMin` | object |  |
| `budgetMax` | number |  |
| `budgetMin` | object |  |
| `createdAt` | string |  |
| `endpointRecipient` | object |  |
| `eventEndpoint` | object |  |
| `furnished` | object |  |
| `geoShapes` | object |  |
| `hidePropertyContact` | boolean |  |
| `includedDepartments[].chefLieu` | string |  |
| `includedDepartments[].departmentCode` | string |  |
| `includedDepartments[].name` | string |  |
| `includedDepartments[].nameClean` | string |  |
| `initiatedFromDashboard` | boolean |  |
| `landSurfaceMax` | object |  |
| `landSurfaceMin` | object |  |
| `lastAlertAt` | object |  |
| `lat` | object |  |
| `lon` | object |  |
| `notificationEnabled` | boolean |  |
| `notificationRecipient` | object |  |
| `pricePerMeterMax` | object |  |
| `pricePerMeterMin` | object |  |
| `propertyTypes[]` | number |  |
| `radius` | object |  |
| `roomMin` | object |  |
| `surfaceMax` | object |  |
| `surfaceMin` | object |  |
| `title` | string |  |
| `token` | string |  |
| `transactionType` | number |  |
| `updatedAt` | string |  |
| `user` | string |  |
| `withCoherentPrice` | boolean |  |
| `withVirtualTour` | object |  |

## Native endpoint

Through the native Melo API, this operation is `GET /searches/:id` (base URL `https://preprod-api.notif.immo`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-search.md) for the provider-specific parameters and requirements.

