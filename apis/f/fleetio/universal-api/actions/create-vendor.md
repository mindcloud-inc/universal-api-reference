# Fleetio: Create Vendor

Creates a new vendor in Fleetio.

```
POST https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/create-vendor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/create-vendor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/create-vendor', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the Vendor. Must be unique. |
| `city` | string | no | The city of the Vendor. |
| `contactEmail` | string | no | The email address of the contact person for the Vendor. |
| `contactName` | string | no | The name of the contact person for the Vendor. |
| `contactPhone` | string | no | The phone number of the contact person for the Vendor. |
| `country` | string | no | The country of the Vendor. |
| `externalId` | string | no | An external ID for the Vendor. Must be unique. |
| `phone` | string | no | The phone number of the Vendor. |
| `postalCode` | string | no | The postal code or ZIP code of the Vendor. |
| `region` | string | no | The region, state, province, or territory of the Vendor. |
| `streetAddress` | string | no | The street address of the Vendor. |
| `streetAddressLine2` | string | no | The second line of the street address of the Vendor. |
| `website` | string | no | The website of the Vendor. |
| `fuel` | boolean | no | Indicates whether the Vendor provides fuel. Will be able to be listed on `Fuel Entries`. |
| `service` | boolean | no | Indicates whether the Vendor provides service. This Vendor will be able to be listed on `Service Entries` and `Work Orders`. |
| `parts` | boolean | no | Indicates whether the Vendor provides parts. This Vendor will be able to be listed on `Parts` and `Purchase Orders`. |
| `vehicle` | boolean | no | Indicates whether the Vendor provides vehicles. This Vendor will be able to be listed on `Acquisitions` and `Vehicles`. |
| `customFields` | object | no | *Full details on working with Custom Fields [here](/docs/overview/custom-fields). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archivedAt": {},
      "city": {},
      "contactEmail": {},
      "contactName": {},
      "contactPhone": {},
      "country": {},
      "createdAt": "string",
      "externalId": {},
      "fuel": true,
      "id": 1,
      "latitude": {},
      "longitude": {},
      "name": "Ava Chen",
      "notes": {},
      "parts": true,
      "phone": {},
      "postalCode": {},
      "region": {},
      "service": true,
      "streetAddress": {},
      "streetAddressLine2": {},
      "updatedAt": "string",
      "vehicle": true,
      "website": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archivedAt` | object |  |
| `city` | object |  |
| `contactEmail` | object |  |
| `contactName` | object |  |
| `contactPhone` | object |  |
| `country` | object |  |
| `createdAt` | string |  |
| `externalId` | object |  |
| `fuel` | boolean |  |
| `id` | number |  |
| `latitude` | object |  |
| `longitude` | object |  |
| `name` | string |  |
| `notes` | object |  |
| `parts` | boolean |  |
| `phone` | object |  |
| `postalCode` | object |  |
| `region` | object |  |
| `service` | boolean |  |
| `streetAddress` | object |  |
| `streetAddressLine2` | object |  |
| `updatedAt` | string |  |
| `vehicle` | boolean |  |
| `website` | object |  |

## Native endpoint

Through the native Fleetio API, this operation is `POST vendors` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vendor.md) for the provider-specific parameters and requirements.

