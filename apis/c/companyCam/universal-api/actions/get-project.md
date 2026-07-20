# CompanyCam: Get Project

Retrieves an existing project from CompanyCam.

```
GET https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CompanyCam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/get-project?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/get-project?${params}`, {
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
| `projectId` | string | yes |  |

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
        "phoneNumber": {},
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
| `primaryContact.phoneNumber` | object |  |
| `primaryContact.projectId` | string |  |
| `primaryContact.updatedAt` | date |  |
| `projectUrl` | string |  |
| `public` | boolean |  |
| `publicUrl` | string |  |
| `slug` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native CompanyCam API, this operation is `GET projects/:projectId` (base URL `https://api.companycam.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

