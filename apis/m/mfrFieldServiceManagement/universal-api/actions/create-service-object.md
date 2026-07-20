# mfr Field Service Management: Create Service Object

Creates a service object in mfr Field Service Management.

```
POST https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/create-service-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mfr Field Service Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/create-service-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/create-service-object', {
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
| `name` | string | yes | Service object name. |
| `externalId` | string | no | External identifier for the service object. |
| `companyId` | string | no | Company ID linked to the service object. |
| `location` | object | no | Service object location object. |
| `contacts[]` | array<object> | no | Contact list for the service object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": 1,
      "createGeoLocation": true,
      "customValues": [
        {}
      ],
      "dateModified": "2026-05-07T12:00:00.000Z",
      "dateOfCreation": "string",
      "externalId": "string",
      "id": 1,
      "isProduct": true,
      "isWarehouse": true,
      "location": {},
      "mappingId": "string",
      "name": "Ava Chen",
      "note": "string",
      "parentServiceObjectId": "string",
      "productId": 1,
      "quickSearch": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | number |  |
| `createGeoLocation` | boolean |  |
| `customValues` | array<object> |  |
| `dateModified` | date |  |
| `dateOfCreation` | string |  |
| `externalId` | string |  |
| `id` | number |  |
| `isProduct` | boolean |  |
| `isWarehouse` | boolean |  |
| `location` | object |  |
| `mappingId` | string |  |
| `name` | string |  |
| `note` | string |  |
| `parentServiceObjectId` | string |  |
| `productId` | number |  |
| `quickSearch` | string |  |
| `version` | number |  |

## Native endpoint

Through the native mfr Field Service Management API, this operation is `POST ServiceObjects` (base URL `https://portal.mobilefieldreport.com/odata`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-service-object.md) for the provider-specific parameters and requirements.

