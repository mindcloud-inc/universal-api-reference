# CompanyCam: Create Project

Creates a new project in CompanyCam.

```
POST https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CompanyCam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/create-project', {
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
| `address.streetAddress1` | string | no |  |
| `coordinates.lat` | number | no | between -3.402823669209385e+38 and 3.402823669209385e+38 |
| `geofence[].lat` | number | no |  |
| `name` | string | yes |  |
| `primaryContact.name` | string | no |  |
| `address` | object | no |  |
| `address.streetAddress2` | string | no |  |
| `coordinates.lon` | number | no | between -3.402823669209385e+38 and 3.402823669209385e+38 |
| `geofence[].lon` | number | no |  |
| `primaryContact.email` | string | no |  |
| `address.city` | string | no |  |
| `primaryContact` | object | no |  |
| `primaryContact.phoneNumber` | string | no |  |
| `address.state` | string | no |  |
| `coordinates` | object | no |  |
| `address.postalCode` | string | no |  |
| `geofence[]` | array<object> | no | (optional) Provide an array of multiple coordinates that effectively "draw" a shape around the address. The most common and easiest approach for a property is to draw a rectangular bounding box. Below is an example geofence for a bounding box approximately 100 meters (330 feet) in each direction of these coordinates: (36.197441, -94.165699). Geofence: 1. Top-Left (36.198441,-94.166699) 2. Top-Right (36.198441,-94.164699) 3. Bottom-Right (36.196441,-94.164699) 4. Bottom-Left (36.196441,-94.166699) |
| `address.country` | string | no | Example: `US`. |

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
        "streetAddress1": "string",
        "streetAddress2": {}
      },
      "archived": true,
      "capturePhotoDeeplink": "https://example.com",
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
      "geofence": [
        {
          "lat": 1,
          "lon": 1
        }
      ],
      "id": "string",
      "integrationRelationId": {},
      "name": "Ava Chen",
      "notepad": {},
      "photoCount": 1,
      "primaryContact": {
        "companyId": "string",
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
      "publicUrl": "https://example.com",
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
| `address.streetAddress2` | object |  |
| `archived` | boolean |  |
| `capturePhotoDeeplink` | string |  |
| `companyId` | string |  |
| `coordinates.lat` | number |  |
| `coordinates.lon` | number |  |
| `createdAt` | date |  |
| `creatorId` | string |  |
| `creatorName` | string |  |
| `creatorType` | string |  |
| `embeddedProjectUrl` | string |  |
| `geofence[].lat` | number |  |
| `geofence[].lon` | number |  |
| `id` | string |  |
| `integrationRelationId` | object |  |
| `name` | string |  |
| `notepad` | object |  |
| `photoCount` | number |  |
| `primaryContact.companyId` | string |  |
| `primaryContact.createdAt` | date |  |
| `primaryContact.email` | string |  |
| `primaryContact.id` | string |  |
| `primaryContact.name` | string |  |
| `primaryContact.phoneNumber` | string |  |
| `primaryContact.projectId` | string |  |
| `primaryContact.updatedAt` | date |  |
| `projectUrl` | string |  |
| `public` | boolean |  |
| `publicUrl` | string |  |
| `slug` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native CompanyCam API, this operation is `POST projects` (base URL `https://api.companycam.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

