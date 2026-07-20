# CompanyCam: Add Label to Project



```
POST https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/add-label-to-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CompanyCam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/add-label-to-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/add-label-to-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project.labels` | string | no | Accepts multiple values as an array. |
| `projectId` | string | yes |  |
| `project` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "city": "string",
        "country": {},
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
      "featureImage": [
        {
          "type": "string",
          "uri": "string",
          "url": "https://example.com"
        }
      ],
      "id": "string",
      "integrationRelationId": {},
      "name": "Ava Chen",
      "notepad": "string",
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
| `address.country` | object |  |
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
| `featureImage[].type` | string |  |
| `featureImage[].uri` | string |  |
| `featureImage[].url` | string |  |
| `id` | string |  |
| `integrationRelationId` | object |  |
| `name` | string |  |
| `notepad` | string |  |
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

Through the native CompanyCam API, this operation is `POST projects/:projectId/labels` (base URL `https://api.companycam.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-label-to-project.md) for the provider-specific parameters and requirements.

