# Fleetio: Retrieve Vendor

Retrieves a specific vendor from Fleetio.

```
GET https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/retrieve-vendor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/retrieve-vendor?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/retrieve-vendor?${params}`, {
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
| `id` | string | yes | The id of the relevant record |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archivedAt": {},
      "city": "string",
      "contactEmail": "ava@example.com",
      "contactName": {},
      "contactPhone": {},
      "country": "string",
      "createdAt": "string",
      "externalId": {},
      "fuel": true,
      "id": 1,
      "latitude": 1,
      "longitude": 1,
      "name": "Ava Chen",
      "notes": {},
      "parts": true,
      "phone": "string",
      "postalCode": "string",
      "region": "string",
      "service": true,
      "streetAddress": "string",
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
| `city` | string |  |
| `contactEmail` | string |  |
| `contactName` | object |  |
| `contactPhone` | object |  |
| `country` | string |  |
| `createdAt` | string |  |
| `externalId` | object |  |
| `fuel` | boolean |  |
| `id` | number |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `name` | string |  |
| `notes` | object |  |
| `parts` | boolean |  |
| `phone` | string |  |
| `postalCode` | string |  |
| `region` | string |  |
| `service` | boolean |  |
| `streetAddress` | string |  |
| `streetAddressLine2` | object |  |
| `updatedAt` | string |  |
| `vehicle` | boolean |  |
| `website` | object |  |

## Native endpoint

Through the native Fleetio API, this operation is `GET vendors/:id` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-vendor.md) for the provider-specific parameters and requirements.

