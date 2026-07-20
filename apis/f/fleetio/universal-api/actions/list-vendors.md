# Fleetio: List Vendors

Retrieves a list of vendors from Fleetio.

```
GET https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/list-vendors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/list-vendors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/list-vendors?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "archivedAt": {},
      "city": "string",
      "contactEmail": {},
      "contactName": "Ava Chen",
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
| `contactEmail` | object |  |
| `contactName` | string |  |
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

Through the native Fleetio API, this operation is `GET vendors` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-vendors.md) for the provider-specific parameters and requirements.

