# Fleetio: Update Vendor

Updates an existing vendor in Fleetio.

```
PUT https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/update-vendor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/update-vendor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/update-vendor', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The id of the relevant record |
| `name` | string | no | The name of the Vendor. Must be unique. |
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fleetio API returns.

## Native endpoint

Through the native Fleetio API, this operation is `PATCH vendors/:id` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-vendor.md) for the provider-specific parameters and requirements.

