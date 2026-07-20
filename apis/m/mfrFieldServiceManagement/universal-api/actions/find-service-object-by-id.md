# mfr Field Service Management: Find Service Object by ID

Finds a service object in mfr Field Service Management by ID.

```
GET https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/find-service-object-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mfr Field Service Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/find-service-object-by-id?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/find-service-object-by-id?${params}`, {
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
| `id` | number | yes |  |

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

Through the native mfr Field Service Management API, this operation is `GET ServiceObjects?$filter=Id eq {{id}}L` (base URL `https://portal.mobilefieldreport.com/odata`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-service-object-by-id.md) for the provider-specific parameters and requirements.

