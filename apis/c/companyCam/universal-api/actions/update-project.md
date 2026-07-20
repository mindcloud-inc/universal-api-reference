# CompanyCam: Update Project



```
PUT https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CompanyCam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/update-project', {
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
| `address.street_address_1` | string | no |  |
| `coordinates.lat` | number | no |  |
| `id` | string | yes | Project Id |
| `name` | string | no |  |
| `address` | object | no |  |
| `address.street_address_2` | string | no |  |
| `coordinates.lon` | number | no |  |
| `geofence[].lat` | number | no |  |
| `address.city` | string | no |  |
| `coordinates` | object | no |  |
| `geofence[].lon` | number | no |  |
| `address.state` | string | no |  |
| `geofence[]` | array<object> | no |  |
| `address.postal_code` | string | no |  |
| `address.country` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "city": "string",
        "country": "string",
        "postalCode": "string",
        "state": "string",
        "streetAddress1": "string"
      },
      "archived": true,
      "companyId": "string",
      "coordinates": {
        "lat": 1,
        "lon": 1
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "creatorName": "Ava Chen",
      "creatorType": "string",
      "embeddedProjectUrl": "https://example.com",
      "featuredImage": [
        {
          "type": "string",
          "url": "https://example.com"
        }
      ],
      "geofence": [
        {
          "lat": 1,
          "lon": 1
        }
      ],
      "id": "string",
      "integrations": [
        {
          "relationId": "string",
          "type": "string"
        }
      ],
      "name": "Ava Chen",
      "notepad": "string",
      "primaryContact": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen",
        "phoneNumber": "string",
        "projectId": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "projectUrl": "https://example.com",
      "public": true,
      "slug": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.city` | string |  |
| `address.country` | string |  |
| `address.postalCode` | string |  |
| `address.state` | string |  |
| `address.streetAddress1` | string |  |
| `archived` | boolean |  |
| `companyId` | string |  |
| `coordinates.lat` | number |  |
| `coordinates.lon` | number |  |
| `createdAt` | date |  |
| `creatorId` | string |  |
| `creatorName` | string |  |
| `creatorType` | string |  |
| `embeddedProjectUrl` | string |  |
| `featuredImage[].type` | string |  |
| `featuredImage[].url` | string |  |
| `geofence[].lat` | number |  |
| `geofence[].lon` | number |  |
| `id` | string |  |
| `integrations[].relationId` | string |  |
| `integrations[].type` | string |  |
| `name` | string |  |
| `notepad` | string |  |
| `primaryContact.createdAt` | date |  |
| `primaryContact.email` | string |  |
| `primaryContact.id` | string |  |
| `primaryContact.name` | string |  |
| `primaryContact.phoneNumber` | string |  |
| `primaryContact.projectId` | string |  |
| `primaryContact.updatedAt` | date |  |
| `projectUrl` | string |  |
| `public` | boolean |  |
| `slug` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native CompanyCam API, this operation is `PUT projects/:id` (base URL `https://api.companycam.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

