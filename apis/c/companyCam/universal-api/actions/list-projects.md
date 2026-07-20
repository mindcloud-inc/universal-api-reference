# CompanyCam: List Projects

Retrieves a list of projects from CompanyCam.

```
GET https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CompanyCam `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/list-projects?${params}`, {
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
| `query` | string | no | An optional value to filter the projects by name or address line 1 |
| `modifiedSince` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "archived": true,
      "public": true,
      "photoCount": 1,
      "companyId": "string",
      "creatorId": "string",
      "creatorType": "string",
      "creatorName": "Ava Chen",
      "address": {
        "streetAddress1": "string",
        "streetAddress2": {},
        "city": "string",
        "state": "string",
        "postalCode": "string",
        "country": {}
      },
      "featureImage": [
        {
          "type": "string",
          "uri": "string",
          "url": "https://example.com"
        }
      ],
      "slug": "string",
      "projectUrl": "https://example.com",
      "publicUrl": "https://example.com",
      "coordinates": {
        "lat": 1,
        "lon": 1
      },
      "primaryContact": {
        "id": "string",
        "email": "ava@example.com",
        "name": "Ava Chen",
        "phoneNumber": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "companyId": "string",
        "projectId": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "embeddedProjectUrl": "https://example.com",
      "capturePhotoDeeplink": "https://example.com",
      "notepad": "string",
      "integrationRelationId": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |
| `archived` | boolean |  |
| `public` | boolean |  |
| `photoCount` | number |  |
| `companyId` | string |  |
| `creatorId` | string |  |
| `creatorType` | string |  |
| `creatorName` | string |  |
| `address.streetAddress1` | string |  |
| `address.streetAddress2` | object |  |
| `address.city` | string |  |
| `address.state` | string |  |
| `address.postalCode` | string |  |
| `address.country` | object |  |
| `featureImage[].type` | string |  |
| `featureImage[].uri` | string |  |
| `featureImage[].url` | string |  |
| `slug` | string |  |
| `projectUrl` | string |  |
| `publicUrl` | string |  |
| `coordinates.lat` | number |  |
| `coordinates.lon` | number |  |
| `primaryContact.id` | string |  |
| `primaryContact.email` | string |  |
| `primaryContact.name` | string |  |
| `primaryContact.phoneNumber` | string |  |
| `primaryContact.createdAt` | date |  |
| `primaryContact.companyId` | string |  |
| `primaryContact.projectId` | string |  |
| `primaryContact.updatedAt` | date |  |
| `createdAt` | date |  |
| `updatedAt` | date |  |
| `embeddedProjectUrl` | string |  |
| `capturePhotoDeeplink` | string |  |
| `notepad` | string |  |
| `integrationRelationId` | object |  |

## Native endpoint

Through the native CompanyCam API, this operation is `GET projects` (base URL `https://api.companycam.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

