# Melo: Update Search

Updates an existing search in Melo.

```
PUT https://connect.mindcloud.co/v1/universal/melo/latest/actions/update-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Melo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/melo/latest/actions/update-search" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "title": "string",
  "transactionType": "1",
  "propertyTypes[]": "0,1",
  "includedDepartments[]": "[/departments/77]",
  "budgetMax": "350000"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/melo/latest/actions/update-search', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "title": "string",
    "transactionType": "1",
    "propertyTypes[]": "0,1",
    "includedDepartments[]": "[/departments/77]",
    "budgetMax": "350000"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Search resource identifier. |
| `title` | string | yes | Search title. |
| `transactionType` | number | yes | Transaction type: 0 sell, 1 rent. Example: `1`. |
| `propertyTypes[]` | array<number> | yes | Property type IDs. Example: `0,1`. |
| `includedDepartments[]` | array<string> | yes | Department resource IDs to include, for example /departments/77. Example: `[/departments/77]`. |
| `budgetMax` | number | yes | Maximum budget amount. Example: `350000`. |

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

Through the native Melo API, this operation is `PUT /searches/:id` (base URL `https://preprod-api.notif.immo`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-search.md) for the provider-specific parameters and requirements.

